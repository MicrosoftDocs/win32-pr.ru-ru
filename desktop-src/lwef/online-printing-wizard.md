---
title: Мастер сетевой печати
description: мастер печати Windows Vista online помогает пользователям заказать отпечатки фотографий от участвующих в интернет-магазинах розничных продавцов.
ms.assetid: 1e73a5d0-2ca8-4eca-846a-bd69eee257cb
keywords:
- Мастер сетевой печати
- значки, Мастер печати в сети
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc402f1fe5853c7a255ea45940d62efcd092c424be6905287315c5cfe5fc7504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975927"
---
# <a name="online-printing-wizard"></a>Мастер сетевой печати

мастер печати Windows Vista online помогает пользователям заказать отпечатки фотографий от участвующих в интернет-магазинах розничных продавцов. Этот мастер разработан таким образом, чтобы его можно было вызывать программно любым приложением, которое хочет предоставить пользователям возможность заказа отпечатков фотографий. мастер печати фотографий доступен в Windows Vista. PIX для Windows

-   [Функции, предоставляемые мастером печати в сети](#features-provided-by-the-online-print-wizard)
-   [Поддерживаемые форматы файлов фотографий](#supported-photo-file-formats)
-   [Программный запуск мастера печати в сети](#programmatically-launching-the-online-print-wizard)
-   [Доступ к значку мастера печати в сети](#accessing-the-online-print-wizard-icon)
-   [Свойства MRU мастера печати в сети](#online-print-wizard-mru-properties)

## <a name="features-provided-by-the-online-print-wizard"></a>Функции, предоставляемые мастером печати в сети

мастер печати Windows Vista online позволяет пользователям упорядочивать отпечатки из выбранных участников интерактивной печати. При вызове мастера:

1.  Принимает файл или список файлов, для которых упорядочиваются отпечатки.
2.  Автоматически извлекает текущий список участвующих в Интернет-магазинах и позволяет пользователю выбрать розничного продавца, с которого будут покупаться фотографии.
3.  Помогает пользователю выполнить процесс или заказать печать.

любое приложение может воспользоваться преимуществами функций, предоставляемых мастером печати Windows Vista Online. Приложению необходимо передать только файл или файлы, для которых будет упорядочена печать, и мастер поможет пользователю выполнить процесс упорядочения.

на следующем рисунке показано, как мастер печати Windows Vista online отображает пример списка участвующих в интернет-магазинах розничных продавцов.

![Мастер печати Windows Vista Online](images/opw.png)

## <a name="supported-photo-file-formats"></a>Поддерживаемые форматы файлов фотографий

мастер печати Windows Vista Online поддерживает любой формат файлов изображений, для которого установлен кодек Windowsного компонента для работы с образами (WIC). Компонент WIC предоставляет несколько стандартных кодеков, в том числе:

-   Точечный рисунок (BMP)
-   GIF
-   Формат значка (ICO)
-   JPEG
-   PNG
-   TIFF
-   Windows Формат фотографии мультимедиа

дополнительные сведения о кодеках wic и wic см. в разделе [Windows imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).

Форматы файлов, поддерживаемые розничными продавцами в сети, отличаются от розничных продавцов. возможно, что конкретный магазин может не поддерживать все форматы файлов, поддерживаемые мастером печати Windows Vista Online. если пользователь пытается заказать отпечатки в формате, который не поддерживается выбранным розничным продавцом, мастер печати Windows Vista Online оповещает пользователя о том, что выбранный магазин не поддерживает формат отправленного файла.

## <a name="programmatically-launching-the-online-print-wizard"></a>Программный запуск мастера печати в сети

чтобы вызвать мастер печати Windows Vista Online, вызовите интерфейс [интерфейс idroptarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) со следующим идентификатором класса (CLSID):


```
CLSID_PublishDropTarget
```



Этот идентификатор CLSID определен в shobjidl. h и shobjidl. idl. файлы, которые будут обрабатывать мастер печати Windows Vista Online, указываются в объекте [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) .

в следующем примере кода показано, как вызвать мастер печати Windows Vista Online.


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



## <a name="accessing-the-online-print-wizard-icon"></a>Доступ к значку мастера печати в сети

мастер печати Windows Vista Online экспортирует значок, который может быть доступен и отображен приложениями, которые его вызывают. на следующем рисунке показан значок мастера Windows Vista Online print Wizard.

![значок мастера печати Windows Vista Online](images/opw-icon.png)

в следующем примере кода показано, как получить индекс для значка мастера печати Windows Vista Online, прочитав свойство **опвикон** .


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



## <a name="online-print-wizard-mru-properties"></a>Свойства MRU мастера печати в сети

мастер печати Windows Vista online определяет три свойства, связанные с последним использованным розничным продавцом (MRU).



| Имя свойства | Значение или функция свойства                                                                                                                                                                                                                                                   |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **мруикон**   | В этом свойстве можно прочитать индекс значка недавно использованного торгового принтера для интерактивной печати.                                                                                                                                                                 |
| **мрунаме**   | В этом свойстве можно прочитать имя последнего использованного торгового модуля для интерактивной печати.                                                                                                                                                                               |
| **усемру**    | Значение **типа Variant** **VT \_** , указывающее, должен ли мастер пропустить страницу выбора розничного принтера в сети и просто использовать недавно использованный Интернет-магазин для интерактивной печати. Присвойте этому свойству значение **Variant \_ true** , чтобы пропустить страницу выбора розничной торговли. |



 

в следующем примере кода показано, как задать свойство усемру, чтобы мастер печати Windows Vista online обойти страницу выбора продавца в режиме «в сети» и автоматически выбрал недавно использованный розничный магазин.


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



В следующем примере кода показано, как считывать свойства Мрунаме и Мруикон.


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



 

 