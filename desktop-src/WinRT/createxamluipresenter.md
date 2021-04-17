---
description: Статическая функция Creator, которая может создать Ксамлуипресентер для поверхности рендеринга в классическом приложении.
ms.assetid: 3160E4C2-39D3-8FF5-ED37-78E645D1AC2E
title: Функция Креатексамлуипресентер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateXamlUIPresenter
api_type:
- DllExport
api_location:
- Windows.UI.Xaml.dll
ms.openlocfilehash: f9561a179ec4501406e26cb2bbc38ea69b64b979
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718172"
---
# <a name="createxamluipresenter-function"></a>Функция Креатексамлуипресентер

Статическая функция Creator, которая может создать [**ксамлуипресентер**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) для поверхности рендеринга в классическом приложении.

## <a name="syntax"></a>Синтаксис


```C++
 static HRESULT WINAPI CreateXamlUIPresenter(
  _In_  IViewObjectPresentNotifySite                 *pPresentSite,
  _Out_ Windows::UI::Xaml::Hosting::IXamlUIPresenter **ppPresenter
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппресентсите* \[ окне\]
</dt> <dd>

Существующий интерфейс размещения. См. раздел **ивиевобжектпресентнотифисите** в документации по Internet Explorer.

</dd> <dt>

*пппресентер* \[ заполняет\]
</dt> <dd>

Интерфейс **\[ Ексклусивето \]** для [**ксамлуипресентер**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Стандартное **значение HRESULT**, **\_ ОК** — успешное завершение.

## <a name="remarks"></a>Комментарии

Для вызова этого метода требуется атрибут **DllImport** от Windows.UI.Xaml.dll.

Этот метод нельзя вызвать из приложения Магазина Windows.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Windows. UI. ксамл-коретипес. idl</dt> </dl> |
| DLL<br/>    | <dl> <dt>Windows.UI.Xaml.dll</dt> </dl>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ксамлуипресентер**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)
</dt> </dl>

 

 
