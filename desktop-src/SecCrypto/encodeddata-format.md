---
description: Возвращает строковое представление закодированных данных.
ms.assetid: d1231e6d-57d7-4b5a-ab37-d4ee1b29cf25
title: Енкодеддата. Format, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Format
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 435d0fdcd6e2bbd8c446c38f97012d820dbe5c7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648967"
---
# <a name="encodeddataformat-method"></a>Енкодеддата. Format, метод

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс асненкодеддата**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Метод **Format** возвращает строковое представление закодированных данных.

## <a name="syntax"></a>Синтаксис


```VB
EncodedData.Format( _
  [ ByVal bMultiLines ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бмултилинес* \[ в необязательное\]
</dt> <dd>

Логическое значение, указывающее, содержит ли возвращаемая строка несколько строк. Если **значение — true**, возвращаемая строка может содержать несколько строк, разделенных **вбкрлф**. Значение по умолчанию равно **False**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Понятная для человека строка, представляющая закодированные данные. Если элемент CAPICOM не понимает закодированные данные, возвращается шестнадцатеричное представление данных.

## <a name="remarks"></a>Комментарии

Формат возвращаемой строки может изменяться в разных версиях элемента CAPICOM. Не полагайтесь на определенный формат в приложении.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**енкодеддата**](encodeddata.md)
</dt> </dl>

 

 
