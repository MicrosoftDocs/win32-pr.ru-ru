---
title: Свойство Enabled Иремотедесктопклиенттаучпоинтер
description: Включена ли функция сенсорного указателя в клиентском элементе управления контейнера приложения RDP.
ms.assetid: f1e2f2f2-1b96-4c5a-b0dd-fd57627c5ec3
ms.tgt_platform: multiple
keywords:
- Включенное свойство службы удаленных рабочих столов
- Включенное свойство службы удаленных рабочих столов, интерфейс Иремотедесктопклиенттаучпоинтер
- Службы удаленных рабочих столов интерфейса Иремотедесктопклиенттаучпоинтер, включенное свойство
topic_type:
- apiref
api_name:
- IRemoteDesktopClientTouchPointer.Enabled
- IRemoteDesktopClientTouchPointer.get_Enabled
- IRemoteDesktopClientTouchPointer.put_Enabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd534a9f8ec77903f196bbdfa10e1823a18dff4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681968"
---
# <a name="iremotedesktopclienttouchpointerenabled-property"></a>Свойство Иремотедесктопклиенттаучпоинтер:: Enabled

Включена ли функция сенсорного указателя в клиентском элементе управления контейнера приложения RDP.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Enabled(
  [in]          VARIANT_BOOL Enabled
);

HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *Enabled
);
```



## <a name="property-value"></a>Значение свойства

**значение true** , если включена функция сенсорного указателя. в противном случае — **значение false**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                      |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>              |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>              |
| IID<br/>                      | IID \_ иремотедесктопклиенттаучпоинтер определен как 260EC22D-8CBC-44B5-9E88-2A37F6C93AE9<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иремотедесктопклиенттаучпоинтер**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer)
</dt> </dl>

 

