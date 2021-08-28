---
title: Ифилллоккбитес — реализация
description: Система предоставляет реализацию Ифилллоккбитес в составе реализации составных файлов.
ms.assetid: a8aed8c5-3c4c-4cce-b568-68031da0edf5
keywords:
- Ифилллоккбитес Стрктд STG, реализация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c095d32bf9a932062b527cd486ee518e099d8de0f0d859caf2f1143e68237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663024"
---
# <a name="ifilllockbytes---implementation"></a>Ифилллоккбитес — реализация

Система предоставляет реализацию [**ифилллоккбитес**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) в составе реализации составных файлов.

При скачивании кода можно создать экземпляр объекта асинхронного составного файла, вызвав [**стгопенасинкдокфилеонифилллоккбитес**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes). Скачивание кода также может создать экземпляр объекта-оболочки асинхронного массива байтов для существующего файла или массива байтов, вызвав либо функцию [**стгжетифилллоккбитесонфиле**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) , либо функцию [**стгжетифилллоккбитесонилоккбитес**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes) .

## <a name="when-to-use"></a>Назначение

Сейчас моникеры URL-адресов являются единственными пользователями реализации асинхронного хранилища COM.

## <a name="remarks"></a>Remarks

Ниже приведены четыре метода реализации [**ифилллоккбитес**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) .

<dl> <dt>

<span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**Ифилллоккбитес:: Филлаппенд**
</dt> <dd>

Записывает новый блок байтов в конец массива байтов. Размер блока указывается в качестве параметра для [**филлаппенд**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend).

</dd> <dt>

<span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**Ифилллоккбитес:: Филлат**
</dt> <dd>

Записывает новый блок данных в указанное расположение в массиве байтов.

</dd> <dt>

<span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**Ифилллоккбитес:: Сетфиллсизе**
</dt> <dd>

Задает размер массива байтов. Возвращает значение E \_ Fail из вызовов [**ILockBytes:: реадат**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat) , пытающихся получить доступ к данным за пределами верхней границы, заданной методом.

</dd> <dt>

<span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**Ифилллоккбитес:: Terminate**
</dt> <dd>

Информирует массив байтов о том, что скачивание было завершено успешно или неудачно.

</dd> </dl>

 

 




