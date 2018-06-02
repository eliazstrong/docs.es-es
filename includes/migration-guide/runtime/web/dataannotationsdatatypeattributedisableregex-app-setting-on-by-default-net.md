### <a name="dataannotationsdatatypeattributedisableregex-app-setting-is-on-by-default-in-net-framework-472"></a><span data-ttu-id="05c21-101">La configuración de aplicación "dataAnnotations:dataTypeAttribute:disableRegEx" está activada de manera predeterminada en .NET Framework 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="05c21-101">"dataAnnotations:dataTypeAttribute:disableRegEx" app setting is on by default in .NET Framework 4.7.2</span></span>

|   |   |
|---|---|
|<span data-ttu-id="05c21-102">Detalles</span><span class="sxs-lookup"><span data-stu-id="05c21-102">Details</span></span>|<span data-ttu-id="05c21-103">En .NET Framework 4.6.1, se incluyó una configuración de aplicación (<code>&quot;dataAnnotations:dataTypeAttribute:disableRegEx&quot;</code>) que permite a los usuarios deshabilitar el uso de expresiones regulares en atributos de tipos de datos (como <xref:System.ComponentModel.DataAnnotations.EmailAddressAttribute?displayProperty=nameWithType>, <xref:System.ComponentModel.DataAnnotations.UrlAttribute?displayProperty=nameWithType> y <xref:System.ComponentModel.DataAnnotations.PhoneAttribute?displayProperty=nameWithType>).</span><span class="sxs-lookup"><span data-stu-id="05c21-103">In .NET Framework 4.6.1, an app setting (<code>&quot;dataAnnotations:dataTypeAttribute:disableRegEx&quot;</code>) was introduced that allows users to disable the use of regular expressions in data type attributes (such as <xref:System.ComponentModel.DataAnnotations.EmailAddressAttribute?displayProperty=nameWithType>, <xref:System.ComponentModel.DataAnnotations.UrlAttribute?displayProperty=nameWithType>, and <xref:System.ComponentModel.DataAnnotations.PhoneAttribute?displayProperty=nameWithType>).</span></span> <span data-ttu-id="05c21-104">Esto ayuda a reducir la vulnerabilidad de la seguridad, ya que se evita la posibilidad de un ataque por denegación de servicio con expresiones regulares específicas.</span><span class="sxs-lookup"><span data-stu-id="05c21-104">This helps to reduce security vulnerability such as avoiding the possibility of a Denial of Service attack using specific regular expressions.</span></span><br/><span data-ttu-id="05c21-105">En .NET Framework 4.6.1, esta configuración de aplicación para deshabilitar el uso de expresiones regulares se estableció en <code>false</code> de manera predeterminada.</span><span class="sxs-lookup"><span data-stu-id="05c21-105">In .NET Framework 4.6.1, this app setting to disable RegEx usage was set to <code>false</code> by default.</span></span> <span data-ttu-id="05c21-106">A partir de .NET Framework 4.7.2, este conmutador de configuración está establecido en <code>true</code> de manera predeterminada para reducir todavía más la vulnerabilidad de la seguridad para aplicaciones web que tengan como objetivo .NET Framework 4.7.2 y versiones superiores.</span><span class="sxs-lookup"><span data-stu-id="05c21-106">Staring with .NET Framework 4.7.2, this config switch is set to <code>true</code> by default to further reduce secure vulnerability for web applications that target .NET Framework 4.7.2 and above.</span></span>|
|<span data-ttu-id="05c21-107">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="05c21-107">Suggestion</span></span>|<span data-ttu-id="05c21-108">Si las expresiones regulares de su aplicación web no funcionan después de actualizar a .NET Framework 4.7.2, puede actualizar el valor de la configuración <code>&quot;dataAnnotations:dataTypeAttribute:disableRegEx&quot;</code> a <code>false</code> para volver al comportamiento anterior.</span><span class="sxs-lookup"><span data-stu-id="05c21-108">If you find that regular expressions in your web application do not work after upgrading to .NET Framework 4.7.2, you can update the value of the <code>&quot;dataAnnotations:dataTypeAttribute:disableRegEx&quot;</code> setting to <code>false</code> to revert to the previous behavior.</span></span><pre><code class="lang-xml">&lt;configuration&gt;&#13;&#10;&lt;appsettings&gt;&#13;&#10;...&#13;&#10;&lt;add key=&quot;dataAnnotations:dataTypeAttribute:disableRegEx&quot; value=&quot;false&quot;/&gt;&#13;&#10;...&#13;&#10;&lt;/appsettings&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|<span data-ttu-id="05c21-109">Ámbito</span><span class="sxs-lookup"><span data-stu-id="05c21-109">Scope</span></span>|<span data-ttu-id="05c21-110">Secundaria</span><span class="sxs-lookup"><span data-stu-id="05c21-110">Minor</span></span>|
|<span data-ttu-id="05c21-111">Versión</span><span class="sxs-lookup"><span data-stu-id="05c21-111">Version</span></span>|<span data-ttu-id="05c21-112">4.7.2</span><span class="sxs-lookup"><span data-stu-id="05c21-112">4.7.2</span></span>|
|<span data-ttu-id="05c21-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="05c21-113">Type</span></span>|<span data-ttu-id="05c21-114">Tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="05c21-114">Runtime</span></span>|
