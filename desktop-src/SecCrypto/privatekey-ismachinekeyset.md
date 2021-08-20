---
description: Возвращает логическое значение, указывающее, принадлежит ли закрытый ключ к набору ключей компьютера.
ms.assetid: ea13ba68-30ae-4aa4-b490-29fd4542c621
title: PrivateKey. Исмачинекэйсет, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsMachineKeyset
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e7fda91354ef1f381bb9e695c82931648f400708744afbc218c6a99238376d86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978180"
---
# <a name="privatekeyismachinekeyset-method"></a>PrivateKey. Исмачинекэйсет, метод

\[Метод **исмачинекэйсет** доступен для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**свойство X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод **исмачинекэйсет** возвращает логическое значение, указывающее, принадлежит ли закрытый ключ к набору ключей компьютера.

## <a name="syntax"></a>Синтаксис


```VB
PrivateKey.IsMachineKeyset()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Если значение — true, закрытый ключ принадлежит набору ключей компьютера.

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

 

 
