---
description: Удаляет хранилище сертификатов, представленное текущим объектом хранилища.
ms.assetid: 274914ee-27a0-4bd6-8510-af897aab3a2d
title: Метод Store. Delete
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41c6417dae5006eb2ecaf64660fd0007cdf37fd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649123"
---
# <a name="storedelete-method"></a>Метод Store. Delete

\[Метод **Delete** доступен для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод **Delete** удаляет [*хранилище сертификатов*](../secgloss/c-gly.md) , представленное текущим объектом [**хранилища**](certificate.md) . Этот метод удаляет только несистемные хранилища.

## <a name="syntax"></a>Синтаксис


```VB
Store.Delete()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Следующие хранилища являются системными хранилищами и не могут быть удалены:

-   My
-   Root
-   Доверие
-   Целостности и доступности
-   усердс
-   TrustedPublisher
-   Запрещено
-   AuthRoot
-   TrustedPeople

Метод **Delete** возвращает ошибку, если вызывается из веб-скрипта.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,1 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Магазин**](store.md)
</dt> <dt>

[**Криптографические объекты**](cryptography-objects.md)
</dt> </dl>

 

 
