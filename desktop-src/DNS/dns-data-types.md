---
title: Типы данных DNS (Винднс. h)
ms.assetid: 652012a5-e45d-4ea6-896a-17e8b1ed4a05
description: 'Дополнительные сведения: типы данных DNS'
keywords:
- IP4_ADDRESS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2caa113670a749029b70df9772d6e2707684b7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264518"
---
# <a name="dns-data-types"></a>Типы данных DNS

Для DNS определены следующие типы данных:


```C++
typedef DWORD IP4_ADDRESS;
```



<dl> <dt>

**IP4- \_ адрес**
</dt> <dd>

Значение, представляющее адрес протокола IP версии 4 (IPv4). Например, разделенный точками десятичный IPv4-адрес ( **127.0.0.1**) представлен в порядке байтов узла как **0x7F000001**.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                |
| Header<br/>                   | <dl> <dt>Винднс. h</dt> </dl> |



 

 





