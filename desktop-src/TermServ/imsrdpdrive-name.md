---
title: Имсрдпдриве имя свойства
description: Возвращает имя диска.
ms.assetid: 5aabb7df-fd46-48aa-ad1d-51da45495782
ms.tgt_platform: multiple
keywords:
- Имя свойства службы удаленных рабочих столов
- Свойство Name службы удаленных рабочих столов, интерфейс Имсрдпдриве
- Службы удаленных рабочих столов интерфейса Имсрдпдриве, свойство Name
topic_type:
- apiref
api_name:
- IMsRdpDrive.Name
- IMsRdpDrive.get_Name
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bde69814f38c39315a02a76bd52b8c3c38baffc2c0a92601ef383cb60b0bc492
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125644"
---
# <a name="imsrdpdrivename-property"></a>Свойство Имсрдпдриве:: Name

Возвращает имя диска.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Name(
  [out] BSTR *pName
);
```



## <a name="property-value"></a>Значение свойства

Имя диска.

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



## <a name="see-also"></a>См. также

<dl> <dt>

[**имсрдпдриве**](imsrdpdrive.md)
</dt> </dl>

 

 





