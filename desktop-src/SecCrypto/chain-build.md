---
description: Создает цепочку проверки сертификатов от конечного сертификата до доверенного корневого сертификата и возвращает логическое значение, указывающее общую достоверность цепочки.
ms.assetid: 878f09ba-d79b-4f14-b4f6-ecb54771f56f
title: 'Метод IChain2:: Build'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.Build
- IChain2.Build
- IChain.Build
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 66ad51d94fdbd361a34e25b4b76289139abb87f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665038"
---
# <a name="ichain2build-method"></a>Метод IChain2:: Build

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод **Build** создает цепочку проверки сертификатов от конечного сертификата до доверенного [*корневого сертификата*](../secgloss/r-gly.md) и возвращает логическое значение, указывающее на общую достоверность цепочки.

## <a name="syntax"></a>Синтаксис


```VB
Chain.Build( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Сертификат* \[ окне\]
</dt> <dd>

Объект [**сертификата**](certificate.md) , представляющий конечный сертификат, на основе которого будет построена цепочка проверки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Логическое значение, указывающее общую достоверность цепочки. Общая достоверность основывается на политике проверки достоверности.

## <a name="remarks"></a>Комментарии

Цепочка создается с помощью свойства [**цертификатестатус. чеккфлаг**](certificatestatus-checkflag.md) , а также политик приложений и сертификатов, заданных объектом [**цертификатестатус**](certificatestatus.md) . Возвращенная коллекция упорядочена; Первый сертификат в коллекции **Certificates. Item**(1) является конечным сертификатом цепочки. Последний сертификат в коллекции **Certificates. Item**(**Certificates. Count**) — это [*корневой сертификат*](../secgloss/r-gly.md) цепочки. **Certificates. Item**(0) представляет всю цепочку.

При каждом вызове метода **Chain. Build** [*состояние*](../secgloss/s-gly.md) объекта [**цепочки**](chain.md) сбрасывается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Криптографические объекты**](cryptography-objects.md)
</dt> <dt>

[**Цепочк**](chain.md)
</dt> </dl>

 

 
