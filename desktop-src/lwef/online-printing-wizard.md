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
# <a name="online-printing-wizard"></a>Мастер сетевой печати

Мастер Интернет-печати в Windows Vista помогает пользователям упорядочивать фотографии из участвующих в Интернет-магазинах розничных продавцов. Этот мастер разработан таким образом, чтобы его можно было вызывать программно любым приложением, которое хочет предоставить пользователям возможность заказа отпечатков фотографий. Мастер печати фотографий доступен в Windows Vista. PIX для Windows

-   [Функции, предоставляемые мастером печати в сети](#features-provided-by-the-online-print-wizard)
-   [Поддерживаемые форматы файлов фотографий](#supported-photo-file-formats)
-   [Программный запуск мастера печати в сети](#programmatically-launching-the-online-print-wizard)
-   [Доступ к значку мастера печати в сети](#accessing-the-online-print-wizard-icon)
-   [Свойства MRU мастера печати в сети](#online-print-wizard-mru-properties)

## <a name="features-provided-by-the-online-print-wizard"></a>Функции, предоставляемые мастером печати в сети

Мастер Интернет-печати в Windows Vista позволяет пользователям упорядочивать отпечатки из набора участвующих в Интернет-магазинах розничных продавцов. При вызове мастера:

1.  Принимает файл или список файлов, для которых упорядочиваются отпечатки.
2.  Автоматически извлекает текущий список участвующих в Интернет-магазинах и позволяет пользователю выбрать розничного продавца, с которого будут покупаться фотографии.
3.  Помогает пользователю выполнить процесс или заказать печать.

Любое приложение может воспользоваться преимуществами средств, предлагаемых мастером Интернет-печати в Windows Vista. Приложению необходимо передать только файл или файлы, для которых будет упорядочена печать, и мастер поможет пользователю выполнить процесс упорядочения.

На следующем рисунке показан пример списка участвующих в Интернет-магазинах розничных продавцов в мастере печати в Windows Vista.

![Мастер печати Windows Vista Online](images/opw.png)

## <a name="supported-photo-file-formats"></a>Поддерживаемые форматы файлов фотографий

Мастер печати Windows Vista Online поддерживает любой формат файлов изображений, для которого установлен кодек компонента Windows Imaging Component (WIC). Компонент WIC предоставляет несколько стандартных кодеков, в том числе:

-   Точечный рисунок (BMP)
-   GIF
-   Формат значка (ICO)
-   JPEG
-   PNG
-   TIFF
-   Формат фотографии Windows Media

Дополнительные сведения о кодеках WIC и WIC см. в разделе [компонент Windows Imaging](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).

Форматы файлов, поддерживаемые розничными продавцами в сети, отличаются от розничных продавцов. возможно, что конкретный магазин может не поддерживать все форматы файлов, поддерживаемые мастером печати в Windows Vista Online. Если пользователь пытается заказать отпечатки в формате, который не поддерживается выбранным розничным продавцом, Мастер печати Windows Vista Online уведомляет пользователя о том, что выбранный магазин не поддерживает формат отправленных файлов.

## <a name="programmatically-launching-the-online-print-wizard"></a>Программный запуск мастера печати в сети

Чтобы вызвать мастер Интернет-печати в Windows Vista, вызовите интерфейс [интерфейс IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) со следующим идентификатором класса (CLSID):


```
CLSID_PublishDropTarget
```



Этот идентификатор CLSID определен в shobjidl. h и shobjidl. idl. Файлы, которые должны быть обработаны мастером печати Windows Vista Online, указываются в объекте [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) .

В следующем примере кода показано, как вызвать мастер печати Windows Vista Online.


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

Мастер Интернет-печати Windows Vista экспортирует значок, который может быть доступен и отображен приложениями, которые его вызывают. На следующем рисунке показан значок мастера Интернет-печати в Windows Vista.

![значок мастера печати Windows Vista Online](images/opw-icon.png)

В следующем примере кода показано, как получить индекс для значка мастера печати в сети Windows Vista, прочитав свойство **опвикон** .


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

Мастер Интернет-печати Windows Vista определяет три свойства, связанные с последним использованным розничным продавцом (MRU).



| Имя свойства | Значение или функция свойства                                                                                                                                                                                                                                                   |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **мруикон**   | В этом свойстве можно прочитать индекс значка недавно использованного торгового принтера для интерактивной печати.                                                                                                                                                                 |
| **мрунаме**   | В этом свойстве можно прочитать имя последнего использованного торгового модуля для интерактивной печати.                                                                                                                                                                               |
| **усемру**    | Значение **типа Variant** **VT \_** , указывающее, должен ли мастер пропустить страницу выбора розничного принтера в сети и просто использовать недавно использованный Интернет-магазин для интерактивной печати. Присвойте этому свойству значение **Variant \_ true** , чтобы пропустить страницу выбора розничной торговли. |



 

В следующем примере кода показано, как задать свойство Усемру, чтобы мастер печати Windows Vista Online обойти страницу выбора розничного принтера в режиме «в сети» и автоматически выбрал недавно использованный розничный магазин.


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



 

 