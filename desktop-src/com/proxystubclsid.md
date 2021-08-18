---
title: проксистубклсид
description: Карты идентификатор IID для идентификатора CLSID в 16-разрядных прокси-библиотеках.
ms.assetid: 07e1e9de-e529-496c-b9f7-e7f799089f02
keywords:
- COM-значение реестра Проксистубклсид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f86db768979a72d2d2f0b8c7a137d6b105f4a52d082ec50c6e78ba271fbca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129996"
---
# <a name="proxystubclsid"></a>проксистубклсид

Карты идентификатор IID для идентификатора CLSID в 16-разрядных прокси-библиотеках.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid = {CLSID}
```

## <a name="remarks"></a>Remarks

Это значение **reg \_ SZ** , указывающее идентификатор CLSID для IID.

При добавлении интерфейсов необходимо использовать эту запись для их регистрации (16-разрядные системы), чтобы OLE мог найти соответствующий код удаленного взаимодействия для установления межпроцессного взаимодействия.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Взаимодействия**](interface-key.md)
</dt> <dt>

[**ProxyStubClsid32**](proxystubclsid32.md)
</dt> </dl>

 

 




