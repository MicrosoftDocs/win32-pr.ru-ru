---
description: В этом разделе описывается реализация компонента в виде библиотеки динамической компоновки (DLL) в Microsoft DirectShow.
ms.assetid: cb935c26-2dc9-4ab3-810d-b63f1018a62a
title: Функции DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b6d1b15df86cf3d7a2eb81080ec02b02a868f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105650417"
---
# <a name="dll-functions"></a><span data-ttu-id="8fb61-103">Функции DLL</span><span class="sxs-lookup"><span data-stu-id="8fb61-103">DLL Functions</span></span>

<span data-ttu-id="8fb61-104">В этом разделе описывается реализация компонента в виде библиотеки динамической компоновки (DLL) в Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="8fb61-104">This topic describes how to implement a component as a dynamic-link library (DLL) in Microsoft DirectShow.</span></span>

<span data-ttu-id="8fb61-105">Библиотека DLL должна реализовывать следующие функции, чтобы ее можно было зарегистрировать, отменить регистрацию и загрузить в память.</span><span class="sxs-lookup"><span data-stu-id="8fb61-105">A DLL must implement the following functions so that it can be registered, unregistered, and loaded into memory.</span></span>

-   <span data-ttu-id="8fb61-106">[*DllMain*](/windows/desktop/Dlls/dllmain): точка входа библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="8fb61-106">[*DllMain*](/windows/desktop/Dlls/dllmain): The DLL entry point.</span></span> <span data-ttu-id="8fb61-107">Имя *DllMain* — это заполнитель для имени определяемой библиотекой функции.</span><span class="sxs-lookup"><span data-stu-id="8fb61-107">The name *DllMain* is a placeholder for the library-defined function name.</span></span> <span data-ttu-id="8fb61-108">В реализации DirectShow используется имя **дллентрипоинт**.</span><span class="sxs-lookup"><span data-stu-id="8fb61-108">The DirectShow implementation uses the name **DllEntryPoint**.</span></span> <span data-ttu-id="8fb61-109">Дополнительные сведения см. в разделе пакет SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="8fb61-109">For more information, see the Platform SDK.</span></span>
-   <span data-ttu-id="8fb61-110">[**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject): создает экземпляр фабрики класса.</span><span class="sxs-lookup"><span data-stu-id="8fb61-110">[**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject): Creates a class factory instance.</span></span> <span data-ttu-id="8fb61-111">Описано в предыдущих разделах.</span><span class="sxs-lookup"><span data-stu-id="8fb61-111">Described in the previous sections.</span></span>
-   <span data-ttu-id="8fb61-112">[**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow): запрашивает возможность безопасной выгрузки библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="8fb61-112">[**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow): Queries whether the DLL can safely be unloaded.</span></span>
-   <span data-ttu-id="8fb61-113">[**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver): создает записи реестра для библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="8fb61-113">[**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver): Creates registry entries for the DLL.</span></span>
-   <span data-ttu-id="8fb61-114">[**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver): удаляет записи реестра для библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="8fb61-114">[**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver): Removes registry entries for the DLL.</span></span>

<span data-ttu-id="8fb61-115">Из них первые три реализуются с помощью DirectShow.</span><span class="sxs-lookup"><span data-stu-id="8fb61-115">Of these, the first three are implemented by DirectShow.</span></span> <span data-ttu-id="8fb61-116">Если шаблон фабрики предоставляет функцию инициализации в переменной-члене [**m \_ лпфнинит**](cfactorytemplate-m-lpfninit.md) , эта функция вызывается из функции точки входа библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="8fb61-116">If your factory template provides an initialization function in the [**m\_lpfnInit**](cfactorytemplate-m-lpfninit.md) member variable, that function is called from inside the DLL entry-point function.</span></span> <span data-ttu-id="8fb61-117">Дополнительные сведения о том, когда система вызывает функцию точки входа библиотеки DLL, см. в разделе [*DllMain*](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="8fb61-117">For more information on when the system calls the DLL entry-point function, see [*DllMain*](/windows/desktop/Dlls/dllmain).</span></span>

<span data-ttu-id="8fb61-118">Необходимо реализовать [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) и [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver), но DirectShow предоставляет функцию с именем [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) , которая выполняет необходимую работу.</span><span class="sxs-lookup"><span data-stu-id="8fb61-118">You must implement [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver), but DirectShow provides a function named [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) that does the necessary work.</span></span> <span data-ttu-id="8fb61-119">Компонент может просто обернуть эту функцию, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="8fb61-119">Your component can simply wrap this function, as shown in the following example:</span></span>


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}

STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



<span data-ttu-id="8fb61-120">Однако в [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) и [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) можно настроить процесс регистрации по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="8fb61-120">However, within [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) you can customize the registration process as needed.</span></span> <span data-ttu-id="8fb61-121">Если ваша библиотека DLL содержит фильтр, может потребоваться дополнительная работа.</span><span class="sxs-lookup"><span data-stu-id="8fb61-121">If your DLL contains a filter, you might need to do some additional work.</span></span> <span data-ttu-id="8fb61-122">Дополнительные сведения см. [в разделе Регистрация фильтров DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="8fb61-122">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

<span data-ttu-id="8fb61-123">В файле определения модуля (DEF) Экспортируйте все функции DLL, кроме функции точки входа.</span><span class="sxs-lookup"><span data-stu-id="8fb61-123">In your module-definition (.def) file, export all the DLL functions except for the entry-point function.</span></span> <span data-ttu-id="8fb61-124">Ниже приведен пример DEF-файла.</span><span class="sxs-lookup"><span data-stu-id="8fb61-124">The following is an example .def file:</span></span>


```C++
EXPORTS
    DllGetClassObject PRIVATE
    DllCanUnloadNow PRIVATE
    DllRegisterServer PRIVATE
    DllUnregisterServer PRIVATE
```



<span data-ttu-id="8fb61-125">Библиотеку DLL можно зарегистрировать с помощью служебной программы Regsvr32.exe.</span><span class="sxs-lookup"><span data-stu-id="8fb61-125">You can register the DLL using the Regsvr32.exe utility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fb61-126">См. также</span><span class="sxs-lookup"><span data-stu-id="8fb61-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fb61-127">Создание библиотеки DLL фильтра DirectShow</span><span class="sxs-lookup"><span data-stu-id="8fb61-127">How to Create a DirectShow Filter DLL</span></span>](how-to-create-a-dll.md)
</dt> </dl>

 

 
