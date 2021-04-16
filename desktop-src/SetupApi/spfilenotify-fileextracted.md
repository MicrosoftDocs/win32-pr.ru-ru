---
description: Уведомление СПФИЛЕНОТИФИ \_ филикстрактед отправляется в подпрограммы обратного вызова с помощью сетупитератекабинет, чтобы указать, что файл был извлечен из CAB-файла или что произошел сбой извлечения, а обработка CAB-файлов была отменена.
ms.assetid: 70ffe06c-e72d-4bb8-a13c-e2946ff72fa6
title: Сообщение SPFILENOTIFY_FILEEXTRACTED (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efdd66c7f218e632ba817d00a6e6c9447052e350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664457"
---
# <a name="spfilenotify_fileextracted-message"></a>\_Сообщение спфиленотифи филикстрактед

Уведомление **спфиленотифи \_ филикстрактед** отправляется в подпрограммы обратного вызова с помощью [**сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) , чтобы указать, что файл был извлечен из CAB-файла или что произошел сбой извлечения, а обработка CAB-файлов была отменена.


```C++
SPFILENOTIFY_FILEEXTRACTED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Параметр1* 
</dt> <dd>

Указатель на структуру [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) , которая содержит сведения о пути для извлеченного файла. Элемент **sourceFile** структуры **FilePath** содержит полный исходный путь к CAB-файлу. Член **TargetFile** предоставляет полный целевой путь к файлу, который должен быть установлен в системе.

</dd> <dt>

*Param2* 
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Подпрограммы обратного вызова CAB-файла должны возвращать одно из следующих значений.



| Код возврата                                                                               | Описание                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**БЕЗ \_ ошибок**</dt> </dl>  | Ошибок не обнаружено, продолжить обработку CAB-файла.<br/>                                                                                                                                |
| <dl> <dt>**Ошибка \_ xxx**</dt> </dl> | Произошла ошибка указанного типа. [**Сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) будет возвращать ноль. [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) вернет указанный код ошибки.<br/> |



 

> [!Note]  
> Нет подпрограммы обратного вызова CAB-файла по умолчанию, предоставляемой API установки. Приложение установки должно предоставить подпрограммы обратного вызова для работы с уведомлениями, отправленными функцией [**сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) .

 

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

[**сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

