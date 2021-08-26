---
description: Представляет контекст планшета.
ms.assetid: d518c42d-c2f6-4776-bea5-fecdfe48e260
title: Интерфейс Итаблетконтекстп
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: da5c26a0a9d7d080a9787fef0b7ba2fdb919e473fd66c989fca478c4ac7d0ac3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883524"
---
# <a name="itabletcontextp-interface"></a>Интерфейс Итаблетконтекстп

Представляет контекст планшета.

## <a name="members"></a>Элементы

Интерфейс **итаблетконтекстп** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Итаблетконтекстп** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **итаблетконтекстп** содержит следующие методы.



| Метод                                                                                           | Описание                                                                     |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**истопмоссук**](itabletcontextp-istopmosthook.md)                                           | Указывает, находится ли контекст планшета в самом верхнем обработчике.<br/>             |
| [**Перекрытие**](itabletcontextp-overlap.md)                                                       | Перемещает контекст планшета на передний или задний план входной очереди.<br/>      |
| [**траккинпутрект**](itabletcontextp-trackinputrect.md)                                         | Обновляет планшет дигитайзер до координат сопоставления расположения окна.<br/> |
| [**усенамедшаредмеморикоммуникатионс**](itabletcontextp-usenamedsharedmemorycommunications.md) | Предоставляет доступ к памяти, используемой между потоками планшета.<br/>             |
| [**усешаредмеморикоммуникатионс**](itabletcontextp-usesharedmemorycommunications.md)           | Предоставляет доступ к памяти, используемой между потоками планшета.<br/>             |



 

## <a name="remarks"></a>Remarks

Разработчики не должны использовать этот интерфейс.

[**усенамедшаредмеморикоммуникатионс**](itabletcontextp-usenamedsharedmemorycommunications.md) доступен только в Windows Vista и более поздних версиях.

В следующем коде показано, как определяется интерфейс **итаблетконтекстп** .

``` syntax
[
    object,
    uuid(22F74D0A-694F-4f47-A5CE-AE08A6409AC8),
    pointer_default(unique)
]
interface ITabletContextP : ITabletContext
{

    HRESULT Overlap([in] BOOL bTop, [out] DWORD *pdwtcid);

    HRESULT GetType([out] CONTEXT_TYPE *pct);

    HRESULT TrackInputRect([out] RECT *prcInput);

    HRESULT IsTopMostHook();

    HRESULT GetEventSink(
        [out] ITabletEventSink **ppSink);

    HRESULT UseSharedMemoryCommunications(
        [in]  DWORD pid,
        [out] DWORD *phEventMoreData,
        [out] DWORD *phEventClientReady,
        [out] DWORD *phMutexAccess,
        [out] DWORD *phFileMapping);

    HRESULT UseNamedSharedMemoryCommunications(
        [in] DWORD pid,
        [in, string] LPCTSTR szSid,
        [in, string] LPCTSTR sdIlSid,
        [out] DWORD *pdwEventMoreDataId,
        [out] DWORD *pdwEventClientReadyId,
        [out] DWORD *pdwMutexAccessId,
        [out] DWORD *pdwFileMappingId);
};
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

