---
title: ProxyStubClsid32
description: Карты идентификатор IID для идентификатора CLSID в 32-разрядных прокси-библиотеках.
ms.assetid: 8d63d2b1-c8ba-4fe8-8025-e7ceee422ee7
keywords:
- COM-значение реестра ProxyStubClsid32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9098ffc7771d3f900489292694ade462a2214e733294a1ed18e6ddb9817692
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309900"
---
# <a name="proxystubclsid32"></a>ProxyStubClsid32

Карты идентификатор IID для идентификатора CLSID в 32-разрядных прокси-библиотеках.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid32 = {CLSID}
```

## <a name="remarks"></a>Remarks

Это значение **reg \_ SZ** , указывающее идентификатор CLSID для IID.

Это обязательная запись, поскольку сопоставление IID-to-CLSID может отличаться для 16-разрядных и 32-разрядных интерфейсов. Сопоставление IID с CLSID зависит от способа упаковки прокси-серверов интерфейса в набор DLL-библиотек прокси.

При добавлении интерфейсов необходимо использовать эту запись для их регистрации (32-разрядные системы), чтобы OLE мог найти соответствующий код удаленного взаимодействия для установления межпроцессного взаимодействия.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)
</dt> <dt>

[**Взаимодействия**](interface-key.md)
</dt> <dt>

[**проксистубклсид**](proxystubclsid.md)
</dt> </dl>

 

 