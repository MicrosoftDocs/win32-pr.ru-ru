---
title: Мастер сетевой печати
description: Мастер Интернет-печати в Windows Vista помогает пользователям упорядочивать фотографии из участвующих в Интернет-магазинах розничных продавцов.
ms.assetid: 1e73a5d0-2ca8-4eca-846a-bd69eee257cb
keywords:
- Мастер сетевой печати
- значки, Мастер печати в сети
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8536eea7a51eddb2dbb46d10c9291a60edfdc74e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337420"
---
# <a name="online-printing-wizard"></a><span data-ttu-id="4c6f0-105">Мастер сетевой печати</span><span class="sxs-lookup"><span data-stu-id="4c6f0-105">Online Printing Wizard</span></span>

<span data-ttu-id="4c6f0-106">Мастер Интернет-печати в Windows Vista помогает пользователям упорядочивать фотографии из участвующих в Интернет-магазинах розничных продавцов.</span><span class="sxs-lookup"><span data-stu-id="4c6f0-106">The Windows Vista Online Printing Wizard helps users order prints of photos from participating online printing retailers.</span></span> <span data-ttu-id="4c6f0-107">Этот мастер разработан таким образом, чтобы его можно было вызывать программно любым приложением, которое хочет предоставить пользователям возможность заказа отпечатков фотографий.</span><span class="sxs-lookup"><span data-stu-id="4c6f0-107">This wizard is designed so that it can be invoked programmatically by any application that wants to offer users the ability to order prints of photos.</span></span> <span data-ttu-id="4c6f0-108">Мастер печати фотографий доступен в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4c6f0-108">The Photo Printing Wizard is available on Windows Vista.</span></span> <span data-ttu-id="4c6f0-109">PIX для Windows</span><span class="sxs-lookup"><span data-stu-id="4c6f0-109">PIX for Windows</span></span>

-   [<span data-ttu-id="4c6f0-110">Функции, предоставляемые мастером печати в сети</span><span class="sxs-lookup"><span data-stu-id="4c6f0-110">Features Provided by the Online Print Wizard</span></span>](#features-provided-by-the-online-print-wizard)
-   [<span data-ttu-id="4c6f0-111">Поддерживаемые форматы файлов фотографий</span><span class="sxs-lookup"><span data-stu-id="4c6f0-111">Supported Photo File Formats</span></span>](#supported-photo-file-formats)
-   [<span data-ttu-id="4c6f0-112">Программный запуск мастера печати в сети</span><span class="sxs-lookup"><span data-stu-id="4c6f0-112">Programmatically Launching the Online Print Wizard</span></span>](#programmatically-launching-the-online-print-wizard)
-   [<span data-ttu-id="4c6f0-113">Доступ к значку мастера печати в сети</span><span class="sxs-lookup"><span data-stu-id="4c6f0-113">Accessing the Online Print Wizard Icon</span></span>](#accessing-the-online-print-wizard-icon)
-   [<span data-ttu-id="4c6f0-114">Свойства MRU мастера печати в сети</span><span class="sxs-lookup"><span data-stu-id="4c6f0-114">Online Print Wizard MRU Properties</span></span>](#online-print-wizard-mru-properties)

## <a name="features-provided-by-the-online-print-wizard"></a><span data-ttu-id="4c6f0-115">Функции, предоставляемые мастером печати в сети</span><span class="sxs-lookup"><span data-stu-id="4c6f0-115">Features Provided by the Online Print Wizard</span></span>

<span data-ttu-id="4c6f0-116">Мастер Интернет-печати в Windows Vista позволяет пользователям упорядочивать отпечатки из набора участвующих в Интернет-магазинах розничных продавцов.</span><span class="sxs-lookup"><span data-stu-id="4c6f0-116">The Windows Vista Online Printing Wizard enables users to order prints from a selection of participating online printing retailers.</span></span> <span data-ttu-id="4c6f0-117">При вызове мастера:</span><span class="sxs-lookup"><span data-stu-id="4c6f0-117">When invoked, the wizard:</span></span>

1.  <span data-ttu-id="4c6f0-118">Принимает файл или список файлов, для которых упорядочиваются отпечатки.</span><span class="sxs-lookup"><span data-stu-id="4c6f0-118">Accepts a file or list of files for which prints are to be ordered.</span></span>
2.  <span data-ttu-id="4c6f0-119">Автоматически извлекает текущий список участвующих в Интернет-магазинах и позволяет пользователю выбрать розничного продавца, с которого будут покупаться фотографии.</span><span class="sxs-lookup"><span data-stu-id="4c6f0-119">Automatically retrieves the current list of participating online printing retailers, and enables the user to select the retailer from which to purchase the photo prints.</span></span>
3.  <span data-ttu-id="4c6f0-120">Помогает пользователю выполнить процесс или заказать печать.</span><span class="sxs-lookup"><span data-stu-id="4c6f0-120">Guides the user through the process or ordering prints.</span></span>

<span data-ttu-id="4c6f0-121">Любое приложение может воспользоваться преимуществами средств, предлагаемых мастером Интернет-печати в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4c6f0-121">Any application can benefit from the features offered by the Windows Vista Online Printing Wizard.</span></span> <span data-ttu-id="4c6f0-122">Приложению необходимо передать только файл или файлы, для которых будет упорядочена печать, и мастер поможет пользователю выполнить процесс упорядочения.</span><span class="sxs-lookup"><span data-stu-id="4c6f0-122">An application need only pass in the file or files for which prints will be ordered, and the wizard guides the user through the ordering process.</span></span>

<span data-ttu-id="4c6f0-123">На следующем рисунке показан пример списка участвующих в Интернет-магазинах розничных продавцов в мастере печати в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4c6f0-123">The following figure shows the Windows Vista Online Printing Wizard displaying an example list of participating online printing retailers.</span></span>

![Мастер печати Windows Vista Online](images/opw.png)

## <a name="supported-photo-file-formats"></a><span data-ttu-id="4c6f0-125">Поддерживаемые форматы файлов фотографий</span><span class="sxs-lookup"><span data-stu-id="4c6f0-125">Supported Photo File Formats</span></span>

<span data-ttu-id="4c6f0-126">Мастер печати Windows Vista Online поддерживает любой формат файлов изображений, для которого установлен кодек компонента Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="4c6f0-126">The Windows Vista Online Printing Wizard supports any image file format for which a Windows Imaging Component (WIC) codec is installed.</span></span> <span data-ttu-id="4c6f0-127">Компонент WIC предоставляет несколько стандартных кодеков, в том числе:</span><span class="sxs-lookup"><span data-stu-id="4c6f0-127">WIC provides several standard codecs, including:</span></span>

-   <span data-ttu-id="4c6f0-128">Точечный рисунок (BMP)</span><span class="sxs-lookup"><span data-stu-id="4c6f0-128">Bitmap (BMP)</span></span>
-   <span data-ttu-id="4c6f0-129">GIF</span><span class="sxs-lookup"><span data-stu-id="4c6f0-129">Graphics Interchange Format (GIF)</span></span>
-   <span data-ttu-id="4c6f0-130">Формат значка (ICO)</span><span class="sxs-lookup"><span data-stu-id="4c6f0-130">Icon Format (ICO)</span></span>
-   <span data-ttu-id="4c6f0-131">JPEG</span><span class="sxs-lookup"><span data-stu-id="4c6f0-131">Joint Photographic Experts Group (JPEG)</span></span>
-   <span data-ttu-id="4c6f0-132">PNG</span><span class="sxs-lookup"><span data-stu-id="4c6f0-132">Portable Network Graphics (PNG)</span></span>
-   <span data-ttu-id="4c6f0-133">TIFF</span><span class="sxs-lookup"><span data-stu-id="4c6f0-133">Tagged Image File Format (TIFF)</span></span>
-   <span data-ttu-id="4c6f0-134">Формат фотографии Windows Media</span><span class="sxs-lookup"><span data-stu-id="4c6f0-134">Windows Media Photo format</span></span>

<span data-ttu-id="4c6f0-135">Дополнительные сведения о кодеках WIC и WIC см. в разделе [компонент Windows Imaging](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="4c6f0-135">For more information about WIC and WIC codecs, see [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).</span></span>

<span data-ttu-id="4c6f0-136">Форматы файлов, поддерживаемые розничными продавцами в сети, отличаются от розничных продавцов. возможно, что конкретный магазин может не поддерживать все форматы файлов, поддерживаемые мастером печати в Windows Vista Online.</span><span class="sxs-lookup"><span data-stu-id="4c6f0-136">File formats supported by online printing retailers vary from retailer to retailer; it is possible that a particular retailer may not support all of the file formats supported by the Windows Vista Online Printing Wizard.</span></span> <span data-ttu-id="4c6f0-137">Если пользователь пытается заказать отпечатки в формате, который не поддерживается выбранным розничным продавцом, Мастер печати Windows Vista Online уведомляет пользователя о том, что выбранный магазин не поддерживает формат отправленных файлов.</span><span class="sxs-lookup"><span data-stu-id="4c6f0-137">If the user attempts to order prints in a format that is not supported by the selected retailer, the Windows Vista Online Printing Wizard notifies the user that the selected retailer does not support the submitted file format.</span></span>

## <a name="programmatically-launching-the-online-print-wizard"></a><span data-ttu-id="4c6f0-138">Программный запуск мастера печати в сети</span><span class="sxs-lookup"><span data-stu-id="4c6f0-138">Programmatically Launching the Online Print Wizard</span></span>

<span data-ttu-id="4c6f0-139">Чтобы вызвать мастер Интернет-печати в Windows Vista, вызовите интерфейс [интерфейс IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) со следующим идентификатором класса (CLSID):</span><span class="sxs-lookup"><span data-stu-id="4c6f0-139">To invoke the Windows Vista Online Printing Wizard, call the [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface with the following class identifier (CLSID):</span></span>


```
CLSID_PublishDropTarget
```



<span data-ttu-id="4c6f0-140">Этот идентификатор CLSID определен в shobjidl. h и shobjidl. idl.</span><span class="sxs-lookup"><span data-stu-id="4c6f0-140">This CLSID is defined in Shobjidl.h and Shobjidl.idl.</span></span> <span data-ttu-id="4c6f0-141">Файлы, которые должны быть обработаны мастером печати Windows Vista Online, указываются в объекте [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="4c6f0-141">The files to be processed by the Windows Vista Online Printing Wizard are specified in an [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) object.</span></span>

<span data-ttu-id="4c6f0-142">В следующем примере кода показано, как вызвать мастер печати Windows Vista Online.</span><span class="sxs-lookup"><span data-stu-id="4c6f0-142">The following code example demonstrates how to invoke the Windows Vista Online Printing Wizard.</span></span>


```
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PublishDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



## <a name="accessing-the-online-print-wizard-icon"></a><span data-ttu-id="4c6f0-143">Доступ к значку мастера печати в сети</span><span class="sxs-lookup"><span data-stu-id="4c6f0-143">Accessing the Online Print Wizard Icon</span></span>

<span data-ttu-id="4c6f0-144">Мастер Интернет-печати Windows Vista экспортирует значок, который может быть доступен и отображен приложениями, которые его вызывают.</span><span class="sxs-lookup"><span data-stu-id="4c6f0-144">The Windows Vista Online Printing Wizard exports an icon that can be accessed and displayed by applications which call it.</span></span> <span data-ttu-id="4c6f0-145">На следующем рисунке показан значок мастера Интернет-печати в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4c6f0-145">The following figure shows the Windows Vista Online Printing Wizard icon.</span></span>

![значок мастера печати Windows Vista Online](images/opw-icon.png)

<span data-ttu-id="4c6f0-147">В следующем примере кода показано, как получить индекс для значка мастера печати в сети Windows Vista, прочитав свойство **опвикон** .</span><span class="sxs-lookup"><span data-stu-id="4c6f0-147">The following code example demonstrates how to retrieve the index for the Windows Vista Online Printing Wizard icon by reading the **OPWIcon** property.</span></span>


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;

spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

// Read the icon index from the properties set. 
CComVariant vtIcon;
int nIndex;
hr = spPropsBag->Read(L"OPWIcon", &vtIcon, NULL);

if SUCCEEDED(hr)
{
    nIndex = vtIcon.lVal;
}
```



## <a name="online-print-wizard-mru-properties"></a><span data-ttu-id="4c6f0-148">Свойства MRU мастера печати в сети</span><span class="sxs-lookup"><span data-stu-id="4c6f0-148">Online Print Wizard MRU Properties</span></span>

<span data-ttu-id="4c6f0-149">Мастер Интернет-печати Windows Vista определяет три свойства, связанные с последним использованным розничным продавцом (MRU).</span><span class="sxs-lookup"><span data-stu-id="4c6f0-149">The Windows Vista Online Printing Wizard defines three properties that are related to the most recently used (MRU) online printing retailer.</span></span>



| <span data-ttu-id="4c6f0-150">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="4c6f0-150">Property Name</span></span> | <span data-ttu-id="4c6f0-151">Значение или функция свойства</span><span class="sxs-lookup"><span data-stu-id="4c6f0-151">Property Value/Function</span></span>                                                                                                                                                                                                                                                   |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c6f0-152">**мруикон**</span><span class="sxs-lookup"><span data-stu-id="4c6f0-152">**MRUIcon**</span></span>   | <span data-ttu-id="4c6f0-153">В этом свойстве можно прочитать индекс значка недавно использованного торгового принтера для интерактивной печати.</span><span class="sxs-lookup"><span data-stu-id="4c6f0-153">The index of the icon for the most recently used online printing retailer can be read from this property.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="4c6f0-154">**мрунаме**</span><span class="sxs-lookup"><span data-stu-id="4c6f0-154">**MRUName**</span></span>   | <span data-ttu-id="4c6f0-155">В этом свойстве можно прочитать имя последнего использованного торгового модуля для интерактивной печати.</span><span class="sxs-lookup"><span data-stu-id="4c6f0-155">The name of the most recently used online printing retailer can be read from this property.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="4c6f0-156">**усемру**</span><span class="sxs-lookup"><span data-stu-id="4c6f0-156">**UseMRU**</span></span>    | <span data-ttu-id="4c6f0-157">Значение **типа Variant** **VT \_** , указывающее, должен ли мастер пропустить страницу выбора розничного принтера в сети и просто использовать недавно использованный Интернет-магазин для интерактивной печати.</span><span class="sxs-lookup"><span data-stu-id="4c6f0-157">A **VARIANT** **VT\_BOOL** value indicating whether the wizard should skip the online printing retailer selection page, and just use the most recently used online printing retailer instead.</span></span> <span data-ttu-id="4c6f0-158">Присвойте этому свойству значение **Variant \_ true** , чтобы пропустить страницу выбора розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="4c6f0-158">Set this property to **VARIANT\_TRUE** to skip the retailer selection page.</span></span> |



 

<span data-ttu-id="4c6f0-159">В следующем примере кода показано, как задать свойство Усемру, чтобы мастер печати Windows Vista Online обойти страницу выбора розничного принтера в режиме «в сети» и автоматически выбрал недавно использованный розничный магазин.</span><span class="sxs-lookup"><span data-stu-id="4c6f0-159">The following code example demonstrates how to set the UseMRU property so the Windows Vista Online Printing Wizard bypasses the online printing retailer selection page and automatically selects the most recently used retailer.</span></span>


```
// A data object that contains the list of photos to order prints for.
IDataObject* pDataObject;

// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Set the UserMRU property to true to skip retailer selection and use 
// the MRU retailer instead.    
CComQIPtr<IPropertyBag> spPropsBag(spDropTarget);
if(spPropsBag) 
{
    VARIANT varTrue = {0};
    varTrue.vt = VT_BOOL;
    varTrue.boolVal = VARIANT_TRUE;
    spPropsBag->Write(L"UseMRU", &varTrue);
}

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);
```



<span data-ttu-id="4c6f0-160">В следующем примере кода показано, как считывать свойства Мрунаме и Мруикон.</span><span class="sxs-lookup"><span data-stu-id="4c6f0-160">The following code example demonstrates how to read the MRUName and MRUIcon properties.</span></span>


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;
spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

CComVariant vtMRUName, vtMRUIconIndex;
CComBSTR bstrMRUName;
int nMRUIconIndex;

// Get the MRU name value.
hr = spPropsBag->Read(L"MRUName", &vtMRUName, NULL);
if SUCCEEDED(hr) 
{
    bstrMRUName = vtMRUName.bstrVal;
}

// Get the MRU icon index value.
hr = spPropsBag->Read(L"MRUIcon", &vtMRUIconIndex, NULL);
if SUCCEEDED(hr)
{
    nMRUIconIndex = vtMRUIconIndex.lVal;
}
```



 

 