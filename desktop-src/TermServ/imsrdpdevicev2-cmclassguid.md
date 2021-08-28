---
title: IMsRdpDeviceV2 Кмклассгуид, свойство
description: Содержит GUID класса установки Configuration Manager для устройства.
ms.assetid: 29ebe2ca-d669-4cc1-8cc1-33490fbb9497
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Кмклассгуид
- Службы удаленных рабочих столов свойства Кмклассгуид, интерфейс IMsRdpDeviceV2
- Службы удаленных рабочих столов интерфейса IMsRdpDeviceV2, свойство Кмклассгуид
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.CmClassGuid
- IMsRdpDeviceV2.get_CmClassGuid
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 372d30ad6dc906b421a6f4a125d3f6fddb88addead17ea27f43369ceee758465
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099394"
---
# <a name="imsrdpdevicev2cmclassguid-property"></a>Свойство IMsRdpDeviceV2:: Кмклассгуид

Содержит GUID класса установки Configuration Manager для устройства.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_CmClassGuid(
  [out, retval] BSTR *pCmClassGuid
);
```



## <a name="property-value"></a>Значение свойства

Идентификатор GUID класса установки Configuration Manager для устройства.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7 с пакетом обновления 1 (SP1)<br/>                                                          |
| Минимальная версия сервера<br/> | Windows Server 2008 R2 с пакетом обновления 1 (SP1)<br/>                                             |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 определен как 5fb94466-7661-42a8-98b7-01904c11668f<br/>      |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IMsRdpDeviceV2**](imsrdpdevicev2.md)
</dt> </dl>

 

 





