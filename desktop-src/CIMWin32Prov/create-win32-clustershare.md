---
description: Создает новый экземпляр Win32 \_ клустершаре.
ms.assetid: a6fde28d-f19e-4a31-8f0d-35927c75a030
ms.tgt_platform: multiple
title: Метод Create класса Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: edaafa00f792cf01b4166d525171cf15b7f781c8c0c943c17377b3bd9b3401dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020592"
---
# <a name="create-method-of-the-win32_clustershare-class"></a>Метод Create \_ класса Win32 клустершаре

Создает новый экземпляр [**Win32 \_ клустершаре**](win32-clustershare.md) .

## <a name="syntax"></a>Синтаксис


```mof
static uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Путь* \[ окне\]
</dt> <dd>

локальный путь к Windows общему ресурсу.

Например, "C: \\ Program Files".

</dd> <dt>

*Имя* \[ окне\]
</dt> <dd>

Псевдоним для пути, настроенного в качестве общего ресурса в компьютерной системе, на которой работает Windows.

Например, "Public".

</dd> <dt>

*Тип* \[ окне\]
</dt> <dd>

Тип ресурса, к которому предоставляется общий доступ. К типам относятся: дисковые накопители, очереди печати, межпроцессное взаимодействие (IPC) и общие устройства.

<dt>

0 (0x0)
</dt> <dd>

Диск

</dd> <dt>

1 (0x1)
</dt> <dd>

Очередь печати

</dd> <dt>

2 (0x2)
</dt> <dd>

Устройство

</dd> <dt>

3 (0x3)
</dt> <dd>

IPC

</dd> <dt>

2147483648 (0x80000000)
</dt> <dd>

Администратор диска

</dd> <dt>

2147483649 (0x80000001)
</dt> <dd>

Администратор очереди печати

</dd> <dt>

2147483650 (0x80000002)
</dt> <dd>

Администратор устройства

</dd> <dt>

2147483651 (0x80000003)
</dt> <dd>

Администратор IPC

</dd> </dl> </dd> <dt>

*MaximumAllowed* \[ в необязательное\]
</dt> <dd>

Максимальное число пользователей, которым разрешено использовать этот ресурс одновременно.

</dd> <dt>

*Описание* \[ в необязательное\]
</dt> <dd>

Описание объекта.

</dd> <dt>

*Пароль* \[ в необязательное\]
</dt> <dd>

Подлежит уточнению

</dd> <dt>

*Доступ к* \[ в необязательное\]
</dt> <dd>

Необязательный встроенный экземпляр класса [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) , который содержит дескриптор безопасности для нового общего ресурса.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                       |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Клустершаре Win32**](win32-clustershare.md)
</dt> </dl>

 

