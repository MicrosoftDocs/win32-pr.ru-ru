---
description: Загружает сертификат подписи из указанного PFX-файла.
ms.assetid: 98963354-c237-40d0-9235-8318728e2c8e
title: Подписывающий. Load, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9a817a95ca825b67b54a41fc674db10bf81b5740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668905"
---
# <a name="signerload-method"></a>Подписывающий. Load, метод

\[Метод **Load** доступен для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс кмссигнер**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Метод **Load** загружает сертификат подписи из указанного PFX-файла.

## <a name="syntax"></a>Синтаксис


```VB
Signer.Load( _
  ByVal FileName, _
  [ ByVal Password ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*FileName* 
</dt> <dd>

Имя PFX-файла, содержащего сертификат подписи.

</dd> <dt>

*Пароль* \[ используемых\]
</dt> <dd>

Строка, содержащая пароль в виде открытого текста, используемый для открытия файла. Для пароля можно использовать до 32 символов Юникода, включая завершающий нуль-символ. Значение по умолчанию — пустая строка. Сведения о защите пароля см. в разделе [обработка паролей](../secbp/handling-passwords.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод загружает первый сертификат из PFX-файла, с которым связан закрытый ключ.

Этот метод вызывает CAPICOM \_ E \_ не \_ разрешен при создании скрипта из веб-приложения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Автор подписи**](signer.md)
</dt> </dl>

 

 
