---
title: проксистубклсид
description: Сопоставляет идентификатор IID с идентификатором CLSID в 16-разрядных прокси-библиотеках.
ms.assetid: 07e1e9de-e529-496c-b9f7-e7f799089f02
keywords:
- COM-значение реестра Проксистубклсид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adfbe319903b2e278be342d169a2e523c952693
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068379"
---
# <a name="proxystubclsid"></a>проксистубклсид

Сопоставляет идентификатор IID с идентификатором CLSID в 16-разрядных прокси-библиотеках.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid = {CLSID}
```

## <a name="remarks"></a>Комментарии

Это значение **reg \_ SZ** , указывающее идентификатор CLSID для IID.

При добавлении интерфейсов необходимо использовать эту запись для их регистрации (16-разрядные системы), чтобы OLE мог найти соответствующий код удаленного взаимодействия для установления межпроцессного взаимодействия.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс**](interface-key.md)
</dt> <dt>

[**ProxyStubClsid32**](proxystubclsid32.md)
</dt> </dl>

 

 




