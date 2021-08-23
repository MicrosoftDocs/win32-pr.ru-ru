---
description: Хранит сведения о контексте планшета.
ms.assetid: a9eadc83-c3dc-42ba-bd4c-24a4a95563ff
title: Интерфейс Итаблетконтекст
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContext
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 3642100b0b974d952dbf9c01d7362ee19f85d48923233e3356ed6e1ec7b58064
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031902"
---
# <a name="itabletcontext-interface"></a>Интерфейс Итаблетконтекст

Хранит сведения о контексте планшета.

## <a name="members"></a>Элементы

Интерфейс **итаблетконтекст** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.

## <a name="remarks"></a>Remarks

В следующем коде определяется интерфейс **итаблетконтекст** .

``` syntax
[
    object,
    uuid(45AAAF04-9D6F-41AE-8ED1-ECD6D4B2F17F),
    pointer_default(unique)
]
interface ITabletContext : IUnknown
{
    HRESULT GetId(
        [out] TABLET_CONTEXT_ID *pTcid);

    HRESULT GetWindow(
        [out] HWND *pHwnd);

    HRESULT GetSettings(
        [out] TABLET_CONTEXT_SETTINGS **ppTCS);

    HRESULT GetTablet(
        [out] ITablet **ppTablet);

    HRESULT Enable(
        [in] CONTEXT_ENABLE_TYPE cet);

    HRESULT GetOptions(
        [out] DWORD *pdwOptions);

    HRESULT GetPacketDescription(
        [out] PACKET_DESCRIPTION **ppPD);

    HRESULT GetStatus(
        [out] DWORD *pdwStatus);

    HRESULT GetInputRect(
        [out] RECT *prcInput);

    HRESULT SetInputRect(
        [in, unique] RECT *prcInput);

    HRESULT SetDevInputRect(
        [in, unique] RECT *prcInput);

    HRESULT GetDevInputRect(
        [out] RECT *prcInput);

    HRESULT SetCapture(void);

    HRESULT ReleaseCapture(void);

    HRESULT SetCursorCapture(
        [in] CURSOR_ID cid);

    HRESULT ReleaseCursorCapture(
        [in] CURSOR_ID cid);

    HRESULT GetPackets(
        [in] ULONG nBegin,
        [in] ULONG nEnd,
        [in, out] ULONG *pcPkts,
        [in] ULONG cbPkts,
        [out, size_is(cbPkts)] BYTE *pbPkts, 
        [out] CURSOR_ID *pCid
    );

    HRESULT PeekPackets(
        [in] ULONG nBegin,
        [in] ULONG nEnd,
        [in, out] ULONG *pcPkts,
        [in] ULONG cbPkts,
        [out, size_is(cbPkts)] BYTE *pbPkts,
        [out] CURSOR_ID * pCid
    );

    HRESULT FlushPackets(
        [in] ULONG nBegin,
        [in] ULONG nEnd
    );

    HRESULT FlushQueue(void);

    HRESULT GetPacketCount(
        [in]  ULONG nBegin,
        [in]  ULONG nEnd,
        [out] ULONG *pcPkts
    );

    HRESULT GetPacketQueueInfo(
        [out] ULONG *pnBegin,
        [out] ULONG *pnEnd,
        [out] ULONG *pcPkts
    );


    HRESULT ForwardPackets(
        [in] ULONG nBegin,
        [in] ULONG nEnd
    );

    HRESULT InjectPackets(
        [in] ULONG cPkts,
        [in] ULONG cbPkts,
        [in, size_is(cbPkts)] BYTE *pbPkts,
        [in, size_is(cPkts)] CURSOR_ID *pCids
    );

    HRESULT ModifyPackets(
        [in] ULONG nBegin,
        [in] ULONG nEnd,
        [in] ULONG cbPkts,
        [in, size_is(cbPkts)] BYTE *pbPkts
    );

    HRESULT ConvertToScreenCoordinates(
        [in] ULONG cPkts,
        [in] ULONG cbPkts,
        [in, size_is(cbPkts)] BYTE *pbPkts,
        [out, size_is(cPkts)] POINT *pPointsInScreen
   );
};  
```

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

