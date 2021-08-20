---
title: Типы данных DNS (Винднс. h)
ms.assetid: 652012a5-e45d-4ea6-896a-17e8b1ed4a05
description: 'Дополнительные сведения: типы данных DNS'
keywords:
- IP4_ADDRESS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81756daaff73e7d5afc1b7c749cd976a9ede09d74ae70eb7db05d9e5d12f2f62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076868"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Винднс. h</dt> </dl> |



 

 





