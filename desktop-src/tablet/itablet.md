---
description: Представляет планшет, подключенный к компьютеру.
ms.assetid: 31e11f7d-5610-4c49-9203-2dc322fbef95
title: Интерфейс Итаблет
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 76fa7baea2713e5a2e5eaae562b6dac29e002fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719589"
---
# <a name="itablet-interface"></a>Интерфейс Итаблет

Представляет планшет, подключенный к компьютеру.

## <a name="members"></a>Элементы

Интерфейс **итаблет** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Итаблет** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **итаблет** содержит следующие методы.



| Метод                                                                 | Описание                                                                           |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**CreateContext**](itablet-createcontext.md)                         | Создает объект контекста, описывающий указанное устройство планшета.<br/>       |
| [**Навести курсор**](/previous-versions/windows/desktop/legacy/aa373535(v=vs.85))                                 | Извлекает указанный объект [**итаблеткурсор**](itabletcursor.md) .<br/>     |
| [**жеткурсоркаунт**](itablet-getcursorcount.md)                       | Извлекает количество объектов Cursor, связанных с планшетом.<br/>         |
| [**жетдефаултконтекстсеттингс**](itablet-getdefaultcontextsettings.md) | Извлекает параметры контекста по умолчанию для планшета.<br/>                     |
| [**жесардварекапс**](itablet-gethardwarecaps.md)                     | Извлекает значение, представляющее возможности устройства планшета.<br/> |
| [**жетмаксинпутрект**](itablet-getmaxinputrect.md)                     | Извлекает прямоугольник, представляющий максимальную область ввода планшета.<br/>    |
| [**GetName**](itablet-getname.md)                                     | Извлекает строку, содержащую имя устройства планшета.<br/>               |
| [**жетплугандплайид**](itablet-getplugandplayid.md)                   | Извлекает строку, содержащую идентификатор самонастраивающийся для устройства планшета.<br/>  |
| [**жетпропертиметрикс**](/previous-versions/windows/desktop/legacy/aa367722(v=vs.85))               | Извлекает данные метрик для указанного свойства.<br/>                       |



 

## <a name="remarks"></a>Комментарии

Разработчики не должны использовать этот интерфейс.

В следующем коде показано, как определяется интерфейс **итаблет** .

``` syntax
[
    object,
   uuid(1CB2EFC3-ABC7-4172-8FCB-3BC9CB93E29F),
    pointer_default(unique)
]
interface ITablet : IUnknown
{
    HRESULT GetDefaultContextSettings(
        [out] TABLET_CONTEXT_SETTINGS **ppTCS);

    HRESULT CreateContext(
        [in] HWND hWnd,
        [in, unique] RECT *prcInput,
        [in] DWORD dwOptions,
        [in, unique] TABLET_CONTEXT_SETTINGS *pTCS,
        [in] CONTEXT_ENABLE_TYPE cet,
        [out] ITabletContext **ppCtx,
        [in, out, unique] TABLET_CONTEXT_ID *pTcid,
        [in, out, unique] PACKET_DESCRIPTION **ppPD,
        [in, unique] ITabletEventSink *pSink);

    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetMaxInputRect(
        [out] RECT *prcInput);

    HRESULT GetHardwareCaps(
        [out] DWORD *pdwCaps);

    HRESULT GetPropertyMetrics(
        [in] REFGUID rguid,
        [out] PROPERTY_METRICS *pPM);

    HRESULT GetPlugAndPlayId(
        [out] LPWSTR *ppwszPPId);

    HRESULT GetCursorCount(
        [out] ULONG *pcCurs);

    HRESULT GetCursor(
        [in] ULONG iCur,
        [out] ITabletCursor **ppCur);
};   
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

