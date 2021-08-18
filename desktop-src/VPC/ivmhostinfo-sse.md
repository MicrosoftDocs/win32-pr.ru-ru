---
title: Свойство SSE Ивмхостинфо (Впккоминтерфацес. h)
description: Определяет, поддерживает ли процессор набор инструкций SSE. | Свойство SSE Ивмхостинфо (Впккоминтерфацес. h)
ms.assetid: 135704db-757a-45b1-884a-5e26ef7d65c7
keywords:
- Виртуальный ПК со свойством SSE
- Свойство SSE Virtual PC, интерфейс Ивмхостинфо
- Интерфейс Ивмхостинфо Virtual PC, свойство SSE
topic_type:
- apiref
api_name:
- IVMHostInfo.SSE
- IVMHostInfo.get_SSE
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355764a018714ef4ce63a817272797aa59dbca59dc060ab18df5f4e9f85baffb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974274"
---
# <a name="ivmhostinfosse-property"></a>Свойство Ивмхостинфо:: SSE

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Определяет, поддерживает ли процессор набор инструкций SSE.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_SSE(
  [out, retval] VARIANT_BOOL *sseEnabled
);
```



## <a name="property-value"></a>Значение свойства

**Значение true** , если инструкции SSE поддерживаются процессором узла; в противном случае — **значение false** .

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>     |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр имеет **значение NULL**.<br/>        |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмхостинфо определен как 5b5cf343-05ad-453b-be99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмхостинфо**](ivmhostinfo.md)
</dt> </dl>

 

