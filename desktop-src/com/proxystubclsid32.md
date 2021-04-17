---
title: ProxyStubClsid32
description: Сопоставляет идентификатор IID с идентификатором CLSID в 32-разрядных прокси-библиотеках.
ms.assetid: 8d63d2b1-c8ba-4fe8-8025-e7ceee422ee7
keywords:
- COM-значение реестра ProxyStubClsid32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d1d70ad2deb4f747ecf57fd12f0707ac8b2b9d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339369"
---
# <a name="proxystubclsid32"></a>ProxyStubClsid32

Сопоставляет идентификатор IID с идентификатором CLSID в 32-разрядных прокси-библиотеках.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid32 = {CLSID}
```

## <a name="remarks"></a>Комментарии

Это значение **reg \_ SZ** , указывающее идентификатор CLSID для IID.

Это обязательная запись, поскольку сопоставление IID-to-CLSID может отличаться для 16-разрядных и 32-разрядных интерфейсов. Сопоставление IID с CLSID зависит от способа упаковки прокси-серверов интерфейса в набор DLL-библиотек прокси.

При добавлении интерфейсов необходимо использовать эту запись для их регистрации (32-разрядные системы), чтобы OLE мог найти соответствующий код удаленного взаимодействия для установления межпроцессного взаимодействия.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)
</dt> <dt>

[**Интерфейс**](interface-key.md)
</dt> <dt>

[**проксистубклсид**](proxystubclsid.md)
</dt> </dl>

 

 