---
title: Программирование ADSI с помощью Java/COM
description: Используя виртуальную машину Майкрософт для Java (Microsoft VM) и Microsoft Java Compiler, вы можете получить доступ ко всем функциям ADSI, предоставляемым через любые COM-компоненты ADSI, из приложения Java/COM.
ms.assetid: eda516b6-0f89-464f-a9d2-9bb4ca70fda5
ms.tgt_platform: multiple
keywords:
- Программирование ADSI с помощью Java/COM AD
- ADSI ADSI, использование, программирование Java/COM для
- ADSI ADSI, пример кода Java
- ADSI ADSI, пример кода Java, привязка к объекту ADSI и вызов методов для этого объекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6899804208f9899823f266bc941bcf3c2dec372
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887503"
---
# <a name="programming-adsi-with-javacom"></a><span data-ttu-id="aebd7-107">Программирование ADSI с помощью Java/COM</span><span class="sxs-lookup"><span data-stu-id="aebd7-107">Programming ADSI with Java/COM</span></span>

<span data-ttu-id="aebd7-108">Используя виртуальную машину Майкрософт для Java (Microsoft VM) и Microsoft Java Compiler, вы можете получить доступ ко всем функциям ADSI, предоставляемым через любые COM-компоненты ADSI, из приложения Java/COM.</span><span class="sxs-lookup"><span data-stu-id="aebd7-108">Using the Microsoft virtual machine for Java (Microsoft VM) and Microsoft Java Compiler, you have access to all the ADSI features exposed through any ADSI COM components, from a Java/COM application.</span></span> <span data-ttu-id="aebd7-109">В следующем примере кода Java показаны элементы, необходимые для привязки к объекту ADSI и вызова методов для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="aebd7-109">The following Java code example shows the elements necessary to bind to an ADSI object and invoke methods on that object.</span></span> <span data-ttu-id="aebd7-110">Необходимые функции API ADSI и методы объектов предоставляются через Activeds.dll.</span><span class="sxs-lookup"><span data-stu-id="aebd7-110">The required ADSI API functions and object methods are exposed through Activeds.dll.</span></span>


```C++
import activeds.*;       // ADSI COM Wrapper classes
import com.ms.com.*;     // to use _Guid data type in COM.

public Class SimpleADSI 
{
    IADs obj;
    String path = "WinNT://domain/machine,computer";
    _Guid riid = IADs.iid;
    public static void main(String args[]) 
    {
        try 
        {
            obj = (IADs)ADsGetObject(path, riid);
            System.out.println( "Object name:  " + obj.getName() );
            System.out.println( "      class:  " + obj.getSchema() );
            System.out.println( "    ADsPath:  " + obj.getADsPath() );
            System.out.println( "     parent:  " + obj.getParent() );
        }
        catch (Exception e) 
        {
            System.out.println( "SimpleADSI Error: " + e.toString() );
        }
    }

    /** @dll.import("activeds", ole) */
    private static native IUnknown ADsGetObject(String path, _Guid riid);
}
```



<span data-ttu-id="aebd7-111">Аргумент в первом операторе **Import** ссылается на классы-оболочки Java, упакованные в Activeds.dll.</span><span class="sxs-lookup"><span data-stu-id="aebd7-111">The argument in the first **import** statement refers to Java Wrapper classes packaged in Activeds.dll.</span></span> <span data-ttu-id="aebd7-112">Используйте Visual J++ для создания классов-оболочек и включения их в проект, следуя приведенной ниже процедуре.</span><span class="sxs-lookup"><span data-stu-id="aebd7-112">Use Visual J++ to create the wrapper classes and include them in your project, following the procedure below.</span></span>

<span data-ttu-id="aebd7-113">**Создание классов-оболочек и их включение в проект**</span><span class="sxs-lookup"><span data-stu-id="aebd7-113">**To create wrapper classes and include them in your project**</span></span>

1.  <span data-ttu-id="aebd7-114">В проекте Visual J++ выберите **добавить оболочку COM...** в меню **проект** .</span><span class="sxs-lookup"><span data-stu-id="aebd7-114">In a Visual J++ project, select **Add Com Wrapper...** from the **Project** menu.</span></span>
2.  <span data-ttu-id="aebd7-115">Выберите "Библиотека типов Active Directory" в списке **установленные компоненты:** в диалоговом окне оболочки COM.</span><span class="sxs-lookup"><span data-stu-id="aebd7-115">Select "Active DS Type Library" from the **Installed Components:** from the COM Wrappers dialog.</span></span> <span data-ttu-id="aebd7-116">Если библиотека типов не отображается в списке, нажмите кнопку **Обзор...** , перейдите в каталог, где хранится активедс. tlb, а затем выберите библиотеку типов.</span><span class="sxs-lookup"><span data-stu-id="aebd7-116">If the type library is not shown in the list box, click the **Browse...** button, navigate to the directory where Activeds.tlb is stored, and then select the type library.</span></span>

<span data-ttu-id="aebd7-117">Visual J++ создает пакет активедс для классов-оболочек Java и включает пакет в путь по умолчанию для проекта.</span><span class="sxs-lookup"><span data-stu-id="aebd7-117">Visual J++ creates the activeds package for the Java Wrapper classes and include the package into the project's default path.</span></span> <span data-ttu-id="aebd7-118">Дополнительные сведения см. в разделе пакет активедс в области **просмотра проекта** в окне Visual J++.</span><span class="sxs-lookup"><span data-stu-id="aebd7-118">For more information, see the activeds package in the **Project Explore** pane on the Visual J++ window.</span></span>

<span data-ttu-id="aebd7-119">Чтобы получить объект ADSI, который не может быть создан одновременно, используйте одну из предоставляемых функций API интерфейса ADSI, например [**адсжетобжект**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) или [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), которые также упаковываются в Activeds.dll.</span><span class="sxs-lookup"><span data-stu-id="aebd7-119">To get an ADSI object that cannot be cocreated, use one of the exposed ADSI API functions, for example, [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) or [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), which are also packaged in Activeds.dll.</span></span> <span data-ttu-id="aebd7-120">Microsoft J/Direct предоставляет доступ к этим и другим собственным API.</span><span class="sxs-lookup"><span data-stu-id="aebd7-120">Microsoft J/Direct provides access to these and other native APIs.</span></span> <span data-ttu-id="aebd7-121">Это продемонстрировано в двух последних строках примера кода выше.</span><span class="sxs-lookup"><span data-stu-id="aebd7-121">This is illustrated by the last two lines of the code example, above.</span></span>

<span data-ttu-id="aebd7-122">При компиляции убедитесь, что расширение языка Майкрософт включено.</span><span class="sxs-lookup"><span data-stu-id="aebd7-122">When compiling, ensure that Microsoft Language Extension is enabled.</span></span> <span data-ttu-id="aebd7-123">Для этого выберите пункт **<project> Свойства...** в меню **проект** в окне проекта Visual J++.</span><span class="sxs-lookup"><span data-stu-id="aebd7-123">To do this, select **<project> Properties...** from the **Project** menu in the Visual J++ project window.</span></span> <span data-ttu-id="aebd7-124">Затем откройте вкладку **Компиляция** в диалоговом окне **<project> Свойства** .</span><span class="sxs-lookup"><span data-stu-id="aebd7-124">Then, click the **Compile** tab in the **<project> Properties** dialog.</span></span> <span data-ttu-id="aebd7-125">Снимите флажок **Отключить расширения языка Майкрософт** .</span><span class="sxs-lookup"><span data-stu-id="aebd7-125">Clear the **Disable Microsoft Language Extensions** check box.</span></span> <span data-ttu-id="aebd7-126">При компиляции из командной строки используйте параметр "/КС-", например:</span><span class="sxs-lookup"><span data-stu-id="aebd7-126">If compiling from the command line, use "/x-" switch, for example:</span></span>

<span data-ttu-id="aebd7-127">**JVC/КС-Симплеадси. Java**</span><span class="sxs-lookup"><span data-stu-id="aebd7-127">**jvc /x- SimpleADSI.java**</span></span>

<span data-ttu-id="aebd7-128">Наконец, чтобы виртуальная машина загрузила COM-компонент, в системном пути должна быть видна библиотека динамической компоновки (DLL).</span><span class="sxs-lookup"><span data-stu-id="aebd7-128">Finally, in order for the virtual machine to load the COM component, the dynamic-link library (DLL) must be visible on the system path.</span></span> <span data-ttu-id="aebd7-129">Если возвращается ошибка "Java. lang. Унсатисфиедлинкеррор", установите путь, чтобы включить путь, содержащий требуемую библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="aebd7-129">If a "java.lang.UnsatisfiedLinkError" error is returned, set the PATH to include the path that contains the required DLL.</span></span> <span data-ttu-id="aebd7-130">Например, если Activeds.dll установлен в c: \\ ADSI \\ lib, выполните в командной строке следующую команду:</span><span class="sxs-lookup"><span data-stu-id="aebd7-130">For example, if Activeds.dll has been installed in c:\\adsi\\lib, issue the following command from the command line:</span></span>

<span data-ttu-id="aebd7-131">**задать путь =% PATH%; в. \\ \\ Библиотека ADSI**</span><span class="sxs-lookup"><span data-stu-id="aebd7-131">**set PATH = %PATH%; c:\\adsi\\lib**</span></span>

 

 




