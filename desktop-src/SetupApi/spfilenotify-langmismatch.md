---
description: Уведомление СПФИЛЕНОТИФИ \_ лангмисматч отправляется в подпрограммы обратного вызова, если язык копируемого файла не совпадает с языком существующего целевого файла.
ms.assetid: dff3969e-5847-4ad5-b7d4-237144bbe8e6
title: Сообщение SPFILENOTIFY_LANGMISMATCH (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3d7828c90dd4dabb8e1cb73a8dcca7ae33ebd3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664456"
---
# <a name="spfilenotify_langmismatch-message"></a>\_Сообщение спфиленотифи лангмисматч

Уведомление **спфиленотифи \_ лангмисматч** отправляется в подпрограммы обратного вызова, если язык копируемого файла не совпадает с языком существующего целевого файла. Его можно отправить в подпрограммы обратного вызова отдельно или вместе с помощью оператора OR с [**спфиленотифи \_ таржетексистс**](spfilenotify-targetexists.md) и/или [**спфиленотифи \_ таржетневер**](spfilenotify-targetnewer.md).


```C++
SPFILENOTIFY_LANGMISMATCH
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) LanguageInfo;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Параметр1* 
</dt> <dd>

Указатель на структуру [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) , содержащую сведения о путях к исходному и целевому файлам.

</dd> <dt>

*Param2* 
</dt> <dd>

Определяет несоответствующие языки. Этот элемент имеет идентификатор языка исходного файла в нижнем слове и идентификатор языка существующего целевого файла в верхнем слове.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Подпрограммы обратного вызова должны возвращать одно из следующих значений.



| Код возврата                                                                          | Описание                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**УСЛОВИЯ**</dt> </dl>  | Скопируйте файл и Перезапишите существующий файл.<br/>               |
| <dl> <dt>**ISFALSE**</dt> </dl> | Пропустить операцию копирования. Не перезаписывайте существующий файл.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Обзор](overview.md)
</dt> <dt>

[Уведомления](notifications.md)
</dt> <dt>

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**сетупдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[**сетупинсталлфиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[**сетупинсталлфиликс**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[**сетупинсталлфроминфсектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




