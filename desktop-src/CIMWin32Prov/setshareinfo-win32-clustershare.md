---
description: Задает параметры общего ресурса.
ms.assetid: 592d0fa6-c865-4f70-89c3-b58204a8c5a6
ms.tgt_platform: multiple
title: Метод Сетшареинфо класса Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 07245e97e091f607d142de57c00109d3671bd81b5f34b9062681229090ff6b50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119439404"
---
# <a name="setshareinfo-method-of-the-win32_clustershare-class"></a>Метод Сетшареинфо \_ класса Win32 клустершаре

Задает параметры общего ресурса.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*MaximumAllowed* \[ в необязательное\]
</dt> <dd>

Максимальное число пользователей, которым разрешено использовать этот ресурс одновременно.

</dd> <dt>

*Описание* \[ в необязательное\]
</dt> <dd>

Описывает ресурс, к которому предоставляется общий доступ.

</dd> <dt>

*Доступ к* \[ в необязательное\]
</dt> <dd>

Дескриптор безопасности для разрешений уровня пользователя. Дескриптор безопасности содержит сведения о разрешениях, владельце и доступе ресурса. Дополнительные сведения см. в разделе [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                       |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Клустершаре Win32**](win32-clustershare.md)
</dt> </dl>

 

