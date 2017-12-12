---
title: Extensiones de tipo (F#)
description: "Obtenga información acerca de cómo las extensiones de tipo de F # permiten que agregar a nuevos miembros a un tipo de objeto previamente definido."
keywords: "visual f#, f#, programación funcional"
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: c9d7ce27-f5ad-4766-b9e9-34187da5bc24
ms.openlocfilehash: f78f8689e95fc1547f1a2b17c615592c00051f7c
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="type-extensions"></a><span data-ttu-id="25785-104">Extensiones de tipo</span><span class="sxs-lookup"><span data-stu-id="25785-104">Type Extensions</span></span>

<span data-ttu-id="25785-105">Extensiones de tipo permiten agregar a nuevos miembros a un tipo de objeto previamente definido.</span><span class="sxs-lookup"><span data-stu-id="25785-105">Type extensions let you add new members to a previously defined object type.</span></span>

## <a name="syntax"></a><span data-ttu-id="25785-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25785-106">Syntax</span></span>

```fsharp
// Intrinsic extension.
type typename with
    member self-identifier.member-name =
        body
    ...
[ end ]

// Optional extension.
type typename with
    member self-identifier.member-name =
        body
    ...
[ end ]
```

## <a name="remarks"></a><span data-ttu-id="25785-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="25785-107">Remarks</span></span>
<span data-ttu-id="25785-108">Hay dos formas de extensiones de tipos que tienen comportamientos y una sintaxis ligeramente diferente.</span><span class="sxs-lookup"><span data-stu-id="25785-108">There are two forms of type extensions that have slightly different syntax and behavior.</span></span> <span data-ttu-id="25785-109">Un *extensión intrínseca* es una extensión que aparece en el mismo espacio de nombres o módulo, en el mismo archivo de origen y en el mismo ensamblado (DLL o archivo ejecutable) como el tipo que se va a extender.</span><span class="sxs-lookup"><span data-stu-id="25785-109">An *intrinsic extension* is an extension that appears in the same namespace or module, in the same source file, and in the same assembly (DLL or executable file) as the type being extended.</span></span> <span data-ttu-id="25785-110">Un *extensión opcional* es una extensión que aparece fuera del espacio de nombres, módulo o ensamblado del tipo que se extiende original.</span><span class="sxs-lookup"><span data-stu-id="25785-110">An *optional extension* is an extension that appears outside the original module, namespace, or assembly of the type being extended.</span></span> <span data-ttu-id="25785-111">Las extensiones intrínsecas aparecen en el tipo cuando el tipo se examina mediante reflexión, pero no así las extensiones opcionales.</span><span class="sxs-lookup"><span data-stu-id="25785-111">Intrinsic extensions appear on the type when the type is examined by reflection, but optional extensions do not.</span></span> <span data-ttu-id="25785-112">Las extensiones opcionales deben estar en módulos y solo están en ámbito cuando se abre el módulo que contiene la extensión.</span><span class="sxs-lookup"><span data-stu-id="25785-112">Optional extensions must be in modules, and they are only in scope when the module that contains the extension is open.</span></span>

<span data-ttu-id="25785-113">En la sintaxis anterior, *typename* representa el tipo que se va a extender.</span><span class="sxs-lookup"><span data-stu-id="25785-113">In the previous syntax, *typename* represents the type that is being extended.</span></span> <span data-ttu-id="25785-114">Se puede extender cualquier tipo que se puede tener acceso, pero el nombre de tipo debe ser un nombre de tipo real, no una abreviatura de tipo.</span><span class="sxs-lookup"><span data-stu-id="25785-114">Any type that can be accessed can be extended, but the type name must be an actual type name, not a type abbreviation.</span></span> <span data-ttu-id="25785-115">Puede definir a varios miembros en una extensión de tipo.</span><span class="sxs-lookup"><span data-stu-id="25785-115">You can define multiple members in one type extension.</span></span> <span data-ttu-id="25785-116">El *self-identifier* representa la instancia del objeto que se invoca, al igual que en los miembros normales.</span><span class="sxs-lookup"><span data-stu-id="25785-116">The *self-identifier* represents the instance of the object being invoked, just as in ordinary members.</span></span>

<span data-ttu-id="25785-117">El `end` palabra clave es opcional en sintaxis ligera.</span><span class="sxs-lookup"><span data-stu-id="25785-117">The `end` keyword is optional in lightweight syntax.</span></span>

<span data-ttu-id="25785-118">Los miembros definidos en las extensiones de tipo pueden usarse al igual que otros miembros de un tipo de clase.</span><span class="sxs-lookup"><span data-stu-id="25785-118">Members defined in type extensions can be used just like other members on a class type.</span></span> <span data-ttu-id="25785-119">Al igual que otros miembros, pueden ser estáticos o miembros de instancia.</span><span class="sxs-lookup"><span data-stu-id="25785-119">Like other members, they can be static or instance members.</span></span> <span data-ttu-id="25785-120">Estos métodos son también se denomina *métodos de extensión*; se denominan propiedades *propiedades de extensión*, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="25785-120">These methods are also known as *extension methods*; properties are known as *extension properties*, and so on.</span></span> <span data-ttu-id="25785-121">Miembros de extensión opcional se compilan en miembros estáticos para los que la instancia de objeto se pasa implícitamente como el primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="25785-121">Optional extension members are compiled to static members for which the object instance is passed implicitly as the first parameter.</span></span> <span data-ttu-id="25785-122">Sin embargo, actúan como si fueran miembros de instancia o los miembros estáticos según cómo se declaran.</span><span class="sxs-lookup"><span data-stu-id="25785-122">However, they act as if they were instance members or static members according to how they are declared.</span></span> <span data-ttu-id="25785-123">Miembros de extensión implícitos se incluyen como miembros del tipo y pueden utilizarse sin restricciones.</span><span class="sxs-lookup"><span data-stu-id="25785-123">Implicit extension members are included as members of the type and can be used without restriction.</span></span>

<span data-ttu-id="25785-124">Métodos de extensión no pueden ser métodos virtuales o abstractos.</span><span class="sxs-lookup"><span data-stu-id="25785-124">Extension methods cannot be virtual or abstract methods.</span></span> <span data-ttu-id="25785-125">Pueden sobrecargar otros métodos del mismo nombre, pero el compilador da preferencia a los métodos de extensión no en el caso de una llamada ambigua.</span><span class="sxs-lookup"><span data-stu-id="25785-125">They can overload other methods of the same name, but the compiler gives preference to non-extension methods in the case of an ambiguous call.</span></span>

<span data-ttu-id="25785-126">Si varias extensiones de tipo intrínseco existen para un tipo, todos los miembros deben ser únicos.</span><span class="sxs-lookup"><span data-stu-id="25785-126">If multiple intrinsic type extensions exist for one type, all members must be unique.</span></span> <span data-ttu-id="25785-127">Las extensiones de tipo opcional, los miembros de las extensiones de tipo diferente en el mismo tipo pueden tener los mismos nombres.</span><span class="sxs-lookup"><span data-stu-id="25785-127">For optional type extensions, members in different type extensions to the same type can have the same names.</span></span> <span data-ttu-id="25785-128">Se producen errores de ambigüedad sólo si el código de cliente abre dos ámbitos diferentes que definen los mismos nombres de miembro.</span><span class="sxs-lookup"><span data-stu-id="25785-128">Ambiguity errors occur only if client code opens two different scopes that define the same member names.</span></span>

<span data-ttu-id="25785-129">En el ejemplo siguiente, un tipo de un módulo tiene una extensión de tipo intrínseco.</span><span class="sxs-lookup"><span data-stu-id="25785-129">In the following example, a type in a module has an intrinsic type extension.</span></span> <span data-ttu-id="25785-130">Al código de cliente fuera del módulo, la extensión de tipo aparece como un miembro normal del tipo en todos los sentidos.</span><span class="sxs-lookup"><span data-stu-id="25785-130">To client code outside the module, the type extension appears as a regular member of the type in all respects.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet3701.fs)]

<span data-ttu-id="25785-131">Puede utilizar extensiones de tipo intrínsecas para separar la definición de un tipo en secciones.</span><span class="sxs-lookup"><span data-stu-id="25785-131">You can use intrinsic type extensions to separate the definition of a type into sections.</span></span> <span data-ttu-id="25785-132">Esto puede ser útil para administrar las definiciones de tipo grande, por ejemplo, para separar el código generado por el compilador y el código creado o agrupar código creados por distintas personas o asociados con una funcionalidad diferente.</span><span class="sxs-lookup"><span data-stu-id="25785-132">This can be useful in managing large type definitions, for example, to keep compiler-generated code and authored code separate or to group together code created by different people or associated with different functionality.</span></span>

<span data-ttu-id="25785-133">En el ejemplo siguiente, una extensión de tipo opcional extiende el `System.Int32` tipo con un método de extensión `FromString` que llama al miembro estático `Parse`.</span><span class="sxs-lookup"><span data-stu-id="25785-133">In the following example, an optional type extension extends the `System.Int32` type with an extension method `FromString` that calls the static member `Parse`.</span></span> <span data-ttu-id="25785-134">El `testFromString` método muestra que el nuevo miembro se llama igual que cualquier miembro de instancia.</span><span class="sxs-lookup"><span data-stu-id="25785-134">The `testFromString` method demonstrates that the new member is called just like any instance member.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet3702.fs)]

<span data-ttu-id="25785-135">El nuevo miembro de instancia aparecerá como cualquier otro método de la `Int32` tipo en IntelliSense, pero solo cuando el módulo que contiene la extensión está abierto o de otra manera en el ámbito.</span><span class="sxs-lookup"><span data-stu-id="25785-135">The new instance member will appear like any other method of the `Int32` type in IntelliSense, but only when the module that contains the extension is open or otherwise in scope.</span></span>

## <a name="generic-extension-methods"></a><span data-ttu-id="25785-136">Métodos de extensión genérico</span><span class="sxs-lookup"><span data-stu-id="25785-136">Generic Extension Methods</span></span>
<span data-ttu-id="25785-137">Antes de F # 3.1, el compilador de F # no admite el uso de C#: aplicar estilo a los métodos de extensión con una variable de tipo genérico, el tipo de matriz, el tipo de tupla o un tipo de función de F # como el parámetro "this".</span><span class="sxs-lookup"><span data-stu-id="25785-137">Before F# 3.1, the F# compiler didn't support the use of C#-style extension methods with a generic type variable, array type, tuple type, or an F# function type as the "this" parameter.</span></span> <span data-ttu-id="25785-138">F # 3.1 admite el uso de estos miembros de extensión.</span><span class="sxs-lookup"><span data-stu-id="25785-138">F# 3.1 supports the use of these extension members.</span></span>

<span data-ttu-id="25785-139">Por ejemplo, en el código de F # 3.1, puede usar los métodos de extensión con firmas similares a la siguiente sintaxis en C#:</span><span class="sxs-lookup"><span data-stu-id="25785-139">For example, in F# 3.1 code, you can use extension methods with signatures that resemble the following syntax in C#:</span></span>

```csharp
static member Method<T>(this T input, T other)
```

<span data-ttu-id="25785-140">Este enfoque es especialmente útil cuando el parámetro de tipo genérico está restringido.</span><span class="sxs-lookup"><span data-stu-id="25785-140">This approach is particularly useful when the generic type parameter is constrained.</span></span> <span data-ttu-id="25785-141">Además, ahora puede declarar miembros de extensión como el siguiente código de F # y definir un conjunto de métodos de extensión adicional y gran riqueza semántica.</span><span class="sxs-lookup"><span data-stu-id="25785-141">Further, you can now declare extension members like this in F# code and define an additional, semantically rich set of extension methods.</span></span> <span data-ttu-id="25785-142">En F #, normalmente se definen a los miembros de extensión como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="25785-142">In F#, you usually define extension members as the following example shows:</span></span>

```fsharp
open System.Collections.Generic

type IEnumerable<'T> with
    /// Repeat each element of the sequence n times
    member xs.RepeatElements(n: int) =
        seq { for x in xs do for i in 1 .. n do yield x }
```

<span data-ttu-id="25785-143">Sin embargo, para un tipo genérico, la variable de tipo puede no ser limitada.</span><span class="sxs-lookup"><span data-stu-id="25785-143">However, for a generic type, the type variable may not be constrained.</span></span> <span data-ttu-id="25785-144">Ahora puede declarar un C#-miembro de extensión de estilo en F # para evitar esta limitación.</span><span class="sxs-lookup"><span data-stu-id="25785-144">You can now declare a C#-style extension member in F# to work around this limitation.</span></span> <span data-ttu-id="25785-145">Cuando se combina este tipo de declaración con la característica en línea de F #, se pueden presentar algoritmos genéricos como miembros de extensión.</span><span class="sxs-lookup"><span data-stu-id="25785-145">When you combine this kind of declaration with the inline feature of F#, you can present generic algorithms as extension members.</span></span>

<span data-ttu-id="25785-146">Considere la siguiente declaración:</span><span class="sxs-lookup"><span data-stu-id="25785-146">Consider the following declaration:</span></span>

```fsharp
[<Extension>]
type ExtraCSharpStyleExtensionMethodsInFSharp () =
    [<Extension>]
    static member inline Sum(xs: IEnumerable<'T>) = Seq.sum xs
```

<span data-ttu-id="25785-147">Mediante el uso de esta declaración, puede escribir código similar al ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="25785-147">By using this declaration, you can write code that resembles the following sample.</span></span>

```fsharp
let listOfIntegers = [ 1 .. 100 ]
let listOfBigIntegers = [ 1I to 100I ]
let sum1 = listOfIntegers.Sum()
let sum2 = listOfBigIntegers.Sum()
```

<span data-ttu-id="25785-148">En este código, el mismo código aritmético genérico se aplica a las listas de dos tipos sin la sobrecarga, al definir a un miembro única extensión.</span><span class="sxs-lookup"><span data-stu-id="25785-148">In this code, the same generic arithmetic code is applied to lists of two types without overloading, by defining a single extension member.</span></span>


## <a name="see-also"></a><span data-ttu-id="25785-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="25785-149">See Also</span></span>
[<span data-ttu-id="25785-150">Referencia del lenguaje F#</span><span class="sxs-lookup"><span data-stu-id="25785-150">F# Language Reference</span></span>](index.md)

[<span data-ttu-id="25785-151">Miembros</span><span class="sxs-lookup"><span data-stu-id="25785-151">Members</span></span>](members/index.md)