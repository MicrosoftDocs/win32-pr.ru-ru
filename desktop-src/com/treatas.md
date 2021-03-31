---
title: треатас
description: Указывает идентификатор CLSID класса, который может эмулировать текущий класс.
ms.assetid: 1d7a1677-738a-4258-9afc-e77bd0dcf40f
keywords:
- COM раздела реестра Треатас
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4340b398d6a98b0445cee932da120e23355b71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888635"
---
# <a name="treatas"></a>треатас

Указывает идентификатор CLSID класса, который может эмулировать текущий класс.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      TreatAs = {CLSID_TreatAs}
```

## <a name="remarks"></a>Комментарии

Это значение **reg \_ SZ** .

Эмуляция — это способность одного приложения открывать и редактировать объект другого класса, сохраняя исходный формат объекта. Разрешение происходит на локальном компьютере, поэтому в случае удаленной активации разрешение происходит на клиентском компьютере с использованием идентификатора CLSID, заданного параметром **треатас**.

DCOM просматривает локальный реестр для **треатас**, даже если вызвать функцию [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) и указать удаленный сервер. Это означает, что если имеется запись **треатас** для класса Class1, которую следует рассматривать как Class2 на локальном компьютере, но вы вызываете **CoCreateInstance** для создания экземпляра Class1 и указываете удаленный сервер, DCOM попытается создать экземпляр класса Class2 на удаленном сервере, даже если Class2 не зарегистрирован на удаленном сервере, что приведет к сбою вызова **CoCreateInstance** .

## <a name="related-topics"></a>См. также

<dl> <dt>

[**аутотреатас**](autotreatas.md)
</dt> <dt>

[**кожеттреатаскласс**](/windows/desktop/api/combaseapi/nf-combaseapi-cogettreatasclass)
</dt> <dt>

[**котреатаскласс**](/windows/desktop/api/Objbase/nf-objbase-cotreatasclass)
</dt> </dl>

 

 




