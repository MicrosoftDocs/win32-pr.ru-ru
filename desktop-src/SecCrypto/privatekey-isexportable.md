---
description: Возвращает логическое значение, указывающее, доступен ли закрытый ключ для экспорта.
ms.assetid: 56e72747-126d-4bb4-ac10-ced0acef388b
title: Метод PrivateKey. Export
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsExportable
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4e4056690be8661628baa1723583489375b37cbb69d2fc9340e218ece87a314b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978430"
---
# <a name="privatekeyisexportable-method"></a>Метод PrivateKey. Export

\[Метод, доступный для **экспорта** , доступен для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**свойство X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод, который может быть **экспортирован** , возвращает логическое значение, указывающее, доступен ли закрытый ключ для экспорта.

## <a name="syntax"></a>Синтаксис


```VB
PrivateKey.IsExportable()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Если значение — true, закрытый ключ помечается как экспортируемый.

## <a name="remarks"></a>Remarks

Возвращаемое значение этого метода зависит от используемого [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP). Этот метод возвращает надежное значение, если используется Microsoft CSP. Если CSP не является CSP Майкрософт, возвращаемое значение не может быть точным.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
