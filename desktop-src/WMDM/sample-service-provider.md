---
title: Образец поставщика услуг
description: Образец поставщика услуг
ms.assetid: bbdeddb5-4ddf-4a61-828c-a9ba7af307ea
keywords:
- Диспетчер устройств Windows Media, примеры
- Диспетчер устройств, примеры
- Диспетчер устройств Windows Media, пример поставщика услуг
- Диспетчер устройств, пример поставщика услуг
- поставщики услуг, примеры
- Примеры, поставщики услуг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8b7e781785944ac1ca390a62303f1149d710d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691235"
---
# <a name="sample-service-provider"></a><span data-ttu-id="c5da7-109">Образец поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="c5da7-109">Sample Service Provider</span></span>

<span data-ttu-id="c5da7-110">Пакет Windows Media диспетчер устройств SDK содержит образец поставщика услуг, который вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="c5da7-110">The Windows Media Device Manager SDK includes a sample service provider for you to use.</span></span> <span data-ttu-id="c5da7-111">Этот поставщик услуг включает класс, сообщающий каждый жесткий диск компьютера, как если бы он был подключенным устройством.</span><span class="sxs-lookup"><span data-stu-id="c5da7-111">This service provider includes a class that reports each hard drive on the computer as if it were an attached device.</span></span> <span data-ttu-id="c5da7-112">Единственным приложением, которое будет использовать этот поставщик услуг, является пример приложения. Проводник Windows не будет видеть "устройства", выданные этим поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="c5da7-112">The only application that will use this service provider is the sample application; Windows Explorer will not see the "devices" reported by this service provider.</span></span> <span data-ttu-id="c5da7-113">Пример поставщика услуг представляет собой COM-объект, созданный на основе ATL.</span><span class="sxs-lookup"><span data-stu-id="c5da7-113">The service provider sample is a COM object built on ATL.</span></span> <span data-ttu-id="c5da7-114">Ниже описано, как использовать образец поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="c5da7-114">The following steps explain how to use the sample service provider:</span></span>

> [!Note]  
> <span data-ttu-id="c5da7-115">Пример поставщика служб реализует очень мало функций, поэтому его не следует использовать для тестирования приложений диспетчер устройств Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c5da7-115">The sample service provider implements very few features, and so it should not be used for testing Windows Media Device Manager applications.</span></span> <span data-ttu-id="c5da7-116">Чтобы протестировать приложение, используйте полностью реализованный поставщик услуг.</span><span class="sxs-lookup"><span data-stu-id="c5da7-116">To test an application, use a fully-implemented service provider.</span></span>

 

-   <span data-ttu-id="c5da7-117">Пример был доставлен с ошибкой в коде, которая приведет к сбою поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="c5da7-117">The sample was shipped with a coding error that will cause the service provider to malfunction.</span></span> <span data-ttu-id="c5da7-118">Чтобы исправить эту ошибку, откройте файл мдспенумстораже. cpp, установленный в папке < *путь установки пакета SDK*  > \\ WMFSDK95 \\ вмдм \\ МДСП \\ мшдсп, перейдите в строку 185 и измените следующую строку:</span><span class="sxs-lookup"><span data-stu-id="c5da7-118">To correct this error, open the MDSPEnumStorage.cpp file installed in the folder < *SDK installation path* >\\WMFSDK95\\WMDM\\mdsp\\mshdsp, go to line 185, and change the following line:</span></span>

`wcsncpy(pStg->m_wcsName, m_wcsPath, dwLen);`

<span data-ttu-id="c5da7-119">На эту:</span><span class="sxs-lookup"><span data-stu-id="c5da7-119">To this:</span></span>

`wcsncpy(pStg->m_wcsName, m_wcsPath, ARRAYSIZE(pStg->m_wcsName));`

1.  <span data-ttu-id="c5da7-120">Скомпилируйте файл MsHDSP.dll.</span><span class="sxs-lookup"><span data-stu-id="c5da7-120">Compile the MsHDSP.dll file.</span></span> <span data-ttu-id="c5da7-121">Это можно сделать с помощью NMAKE или Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c5da7-121">You can do this using either NMAKE or Visual Studio.</span></span> <span data-ttu-id="c5da7-122">Сведения о компиляции приложения см. в разделе [Компиляция примера поставщика услуг с помощью NMAKE](compiling-the-sample-service-provider-using-nmake.md) или [Компиляция примера поставщика услуг с помощью Visual Studio](compiling-the-sample-service-provider-using-visual-studio.md) .</span><span class="sxs-lookup"><span data-stu-id="c5da7-122">See [Compiling the Sample Service Provider Using NMAKE](compiling-the-sample-service-provider-using-nmake.md) or [Compiling the Sample Service Provider Using Visual Studio](compiling-the-sample-service-provider-using-visual-studio.md) to learn how to compile the application.</span></span>
2.  <span data-ttu-id="c5da7-123">Зарегистрируйте MsHDSP.dll с помощью regsvr32.</span><span class="sxs-lookup"><span data-stu-id="c5da7-123">Register MsHDSP.dll using regsvr32.</span></span> <span data-ttu-id="c5da7-124">Следующая строка, введенная в окно командной строки в той же папке, что и MsHDSP.dll, зарегистрирует образец поставщика услуг:</span><span class="sxs-lookup"><span data-stu-id="c5da7-124">The following line, typed into a command-prompt window in the same folder as MsHDSP.dll, will register the sample service provider:</span></span>

    ```C++
    regsvr32 mshdsp.dll
    ```

    

    <span data-ttu-id="c5da7-125">Чтобы отключить олицетворение устройства, введите в командной строке следующую строку:</span><span class="sxs-lookup"><span data-stu-id="c5da7-125">To stop impersonating a device, enter the following line at the command prompt:</span></span>

    ```C++
    regsvr32 /u mshdsp.dll
    ```

    

3.  <span data-ttu-id="c5da7-126">Съемные устройства, олицетворенные с помощью этой библиотеки DLL, могут рассматриваться только в примере приложения, поставляемого с этим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="c5da7-126">The removable devices impersonated by this DLL can only be seen by the sample application shipped with this SDK.</span></span> <span data-ttu-id="c5da7-127">Скомпилируйте пример приложения с помощью одного из методов, описанных в [примере классического приложения](sample-desktop-application.md).</span><span class="sxs-lookup"><span data-stu-id="c5da7-127">Compile the sample application using one of the methods described in [Sample Desktop Application](sample-desktop-application.md).</span></span>
4.  <span data-ttu-id="c5da7-128">Чтобы выполнить отладку поставщика услуг с помощью Visual Studio, откройте поставщик службы в Visual Studio и выберите команду **запустить** в меню **Отладка** .</span><span class="sxs-lookup"><span data-stu-id="c5da7-128">To debug the service provider with Visual Studio, open the service provider in Visual Studio and select **Start** on the **Debug** menu.</span></span> <span data-ttu-id="c5da7-129">Во всплывающем диалоговом окне перейдите к образцу приложения, созданному на предыдущем шаге, и нажмите кнопку **ОК**, и поставщик услуг начнет работать в режиме отладки.</span><span class="sxs-lookup"><span data-stu-id="c5da7-129">In the popup dialog box, browse to the sample application you built in the preceding step, and click **OK**, and the service provider will begin running in debug mode.</span></span>

    <span data-ttu-id="c5da7-130">Чтобы запустить поставщик службы без отладки в Visual Studio, просто зарегистрируйте msdhsp.dll и запустите пример приложения для настольных систем, которое поставляется вместе с пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="c5da7-130">To run the service provider without debugging in Visual Studio, simply register the msdhsp.dll and run the sample desktop application that ships with the SDK.</span></span> <span data-ttu-id="c5da7-131">Пример классического приложения запускает образец поставщика услуг автоматически.</span><span class="sxs-lookup"><span data-stu-id="c5da7-131">The sample desktop application runs the sample service provider automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5da7-132">См. также</span><span class="sxs-lookup"><span data-stu-id="c5da7-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5da7-133">**Примеры**</span><span class="sxs-lookup"><span data-stu-id="c5da7-133">**Samples**</span></span>](samples.md)
</dt> </dl>

 

 




