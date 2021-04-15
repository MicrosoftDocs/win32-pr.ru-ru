---
description: Таблица Мсифилехаш используется для хранения 128-разрядного хэша исходного файла, предоставленного пакетом установщик Windows. Хэш разбивается на 4 32-разрядные значения и хранится в отдельных столбцах таблицы.
ms.assetid: 972a2784-418d-4cb3-b13c-df89b079e94c
title: Таблица Мсифилехаш
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86acb299e5d7f099a8d49affc64810d128e88369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662371"
---
# <a name="msifilehash-table"></a>Таблица Мсифилехаш

Таблица **мсифилехаш** используется для хранения 128-разрядного хэша исходного файла, предоставленного пакетом установщик Windows. Хэш разбивается на 4 32-разрядные значения и хранится в отдельных столбцах таблицы.

Установщик Windows может использовать хэширование файлов в качестве средства для обнаружения и устранения ненужного копирования файлов. Хэш файла, хранящийся в таблице **мсифилехаш** , может сравниваться с хэшем существующего файла на компьютере пользователя, полученного путем вызова [**мсижетфилехаш**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha). Таблицу **мсифилехаш** можно использовать только с файлами без версий.

Таблица **мсифилехаш** содержит следующие столбцы.



| Столбец    | Type                               | Ключ | Допускает значения NULL |
|-----------|------------------------------------|-----|----------|
| Файл\_    | [Идентификатор](identifier.md)       | Да   | Нет        |
| Параметры   | [Integer](integer.md)             | Нет   | Нет        |
| HashPart1 | [даублеинтежер](doubleinteger.md) | Нет   | Нет        |
| HashPart2 | [даублеинтежер](doubleinteger.md) | Нет   | Нет        |
| HashPart3 | [даублеинтежер](doubleinteger.md) | Нет   | Нет        |
| Hashpart4 | [даублеинтежер](doubleinteger.md) | Нет   | Нет        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_
</dt> <dd>

Внешний ключ к [таблице файлов](file-table.md). 72 строка char.

</dd> <dt>

<span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Параметры
</dt> <dd>

Этот столбец должен быть равен 0 и зарезервирован для использования в будущем.

</dd> <dt>

<span id="HashPart1"></span><span id="hashpart1"></span><span id="HASHPART1"></span>HashPart1
</dt> <dd>

Первые 32 бит хэша. Хэш файла, указанный в этом поле, должен быть получен путем вызова [**мсижетфилехаш**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) или [**метода FileHash**](installer-filehash.md). Не используйте другие методы.

</dd> <dt>

<span id="HashPart2"></span><span id="hashpart2"></span><span id="HASHPART2"></span>HashPart2
</dt> <dd>

Второй 32 бит хэша. Хэш файла, указанный в этом поле, должен быть получен путем вызова [**мсижетфилехаш**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) или [**метода FileHash**](installer-filehash.md). Не используйте другие методы хэширования.

</dd> <dt>

<span id="HashPart3"></span><span id="hashpart3"></span><span id="HASHPART3"></span>HashPart3
</dt> <dd>

Третий 32 бит хэша. Хэш файла, указанный в этом поле, должен быть получен путем вызова [**мсижетфилехаш**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) или [**метода FileHash**](installer-filehash.md). Не используйте другие методы.

</dd> <dt>

<span id="HashPart4"></span><span id="hashpart4"></span><span id="HASHPART4"></span>HashPart4
</dt> <dd>

Четвертый 32 бит хэша. Хэш файла, указанный в этом поле, должен быть получен путем вызова [**мсижетфилехаш**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) или [**метода FileHash**](installer-filehash.md). Не используйте другие методы.

</dd> </dl>

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE60](ice60.md)  
[ICE66](ice66.md)  
</dl>

## <a name="related-topics"></a>См. также

<dl> <dt>

[**мсижетфилехаш**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> <dt>

[Управление версиями файлов по умолчанию](default-file-versioning.md)
</dt> </dl>

 

 



