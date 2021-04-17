---
title: Имсрдпдриве Редиректионстате, свойство
description: Указывает состояние перенаправления диска.
ms.assetid: 05333671-460d-4c07-8b7e-fbb7bc215353
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Редиректионстате
- Службы удаленных рабочих столов свойства Редиректионстате, интерфейс Имсрдпдриве
- Службы удаленных рабочих столов интерфейса Имсрдпдриве, свойство Редиректионстате
topic_type:
- apiref
api_name:
- IMsRdpDrive.RedirectionState
- IMsRdpDrive.get_RedirectionState
- IMsRdpDrive.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7561190e976e0b8190553376f5e9f7a5b2de2550
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415860"
---
# <a name="imsrdpdriveredirectionstate-property"></a>Свойство Имсрдпдриве:: Редиректионстате

Указывает состояние перенаправления диска.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_RedirectionState(
  [in]  VARIANT_BOOL vboolRedirState
);

HRESULT get_RedirectionState(
  [out] VARIANT_BOOL *pvboolRedirState
);
```



## <a name="property-value"></a>Значение свойства

Присвойте этому параметру значение **Variant \_ false**. для отключения перенаправления или **варианта \_ true**. для включения перенаправления.

## <a name="error-codes"></a>Коды ошибок

Если метод выполнен успешно, возвращается значение **S \_ OK** . Любое другое значение **HRESULT** указывает на сбой вызова.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ имсрдпдриве определен как d28b5458-f694-47a8-8e61-40356a767e46<br/>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имсрдпдриве**](imsrdpdrive.md)
</dt> </dl>

 

 





