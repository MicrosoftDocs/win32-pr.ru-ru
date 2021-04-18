---
description: Метод Опендатабасе объекта Installer открывает существующую базу данных или создает новую, возвращая объект базы данных. Он выдает ошибку, если не удается успешно создать и открыть объект базы данных.
ms.assetid: a77b3954-db27-41a0-8f8b-2654766bde6a
title: Метод Installer. Опендатабасе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenDatabase
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 13256f0bbe2d5adad61c46ea091e8207f1a9351b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651596"
---
# <a name="installeropendatabase-method"></a>Метод Installer. Опендатабасе

Метод **опендатабасе** объекта [**Installer**](installer-object.md) открывает существующую базу данных или создает новую, возвращая объект [**базы данных**](database-object.md) . Он выдает ошибку, если не удается успешно создать и открыть объект **базы данных** .

## <a name="syntax"></a>Синтаксис


```JScript
Installer.OpenDatabase(
  name,
  openMode
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*name* 
</dt> <dd>

Обязательная строка, содержащая имя пути к базе данных. Если указана пустая строка, создается временная база данных, которая не сохраняется.

</dd> <dt>

*openMode* 
</dt> <dd>

Параметр из следующего списка или строка, содержащая имя нового файла выходной базы данных, в который необходимо выполнить запись после фиксации.



| Параметр                                                                                                                                                                                                                                                                                                                   | Значение                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiOpenDatabaseModeReadOnly"></span><span id="msiopendatabasemodereadonly"></span><span id="MSIOPENDATABASEMODEREADONLY"></span><dl> <dt>**мсиопендатабасемодереадонли**</dt> <dt>0</dt> </dl>                 | Открывает базу данных только для чтения без постоянных изменений.<br/>                                                                                                           |
| <span id="msiOpenDatabaseModeTransact"></span><span id="msiopendatabasemodetransact"></span><span id="MSIOPENDATABASEMODETRANSACT"></span><dl> <dt>**мсиопендатабасемодетрансакт**</dt> <dt>1</dt> </dl>                 | Открывает базу данных для чтения и записи в режиме транзакций.<br/>                                                                                                             |
| <span id="msiOpenDatabaseModeDirect"></span><span id="msiopendatabasemodedirect"></span><span id="MSIOPENDATABASEMODEDIRECT"></span><dl> <dt>**мсиопендатабасемодедирект**</dt> <dt>2</dt> </dl>                         | Открывает базу данных с прямым чтением и записью без транзакции.<br/>                                                                                                      |
| <span id="msiOpenDatabaseModeCreate"></span><span id="msiopendatabasemodecreate"></span><span id="MSIOPENDATABASEMODECREATE"></span><dl> <dt>**мсиопендатабасемодекреате**</dt> <dt>3</dt> </dl>                         | Создает новую базу данных, доступную для чтения и записи в режиме Transact.<br/>                                                                                                            |
| <span id="msiOpenDatabaseModeCreateDirect"></span><span id="msiopendatabasemodecreatedirect"></span><span id="MSIOPENDATABASEMODECREATEDIRECT"></span><dl> <dt>**мсиопендатабасемодекреатедирект**</dt> <dt>4</dt> </dl> | Создает новую базу данных, прямой режим — чтение и запись.<br/>                                                                                                              |
| <span id="msiOpenDatabaseModeListScript"></span><span id="msiopendatabasemodelistscript"></span><span id="MSIOPENDATABASEMODELISTSCRIPT"></span><dl> <dt>**мсиопендатабасемоделистскрипт**</dt> <dt>5</dt> </dl>         | Открывает базу данных для просмотра файлов скриптов объявления, например файлов, создаваемых методом [**креатеадвертисескрипт**](installer-createadvertisescript.md) .<br/> |
| <span id="msiOpenDatabaseModePatchFile"></span><span id="msiopendatabasemodepatchfile"></span><span id="MSIOPENDATABASEMODEPATCHFILE"></span><dl> <dt>**мсиопендатабасемодепатчфиле**</dt> <dt>32</dt> </dl>            | Добавляет этот флаг для указания файла исправления.<br/>                                                                                                                     |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

При открытии базы данных в качестве выходных данных другой базы данных информационный поток выходной базы данных фактически является зеркальной базой данных, предназначенной только для чтения, и поэтому не может быть изменен. Кроме того, она не сохраняется в базе данных. Чтобы создать или изменить сводные данные для выходной базы данных, ее необходимо закрыть и повторно открыть.

Чтобы внести и сохранить изменения в базе данных, сначала откройте базу данных в Transaction (Мсиопендатабасемодетрансакт), создайте (Мсиопендатабасемодекреате или Мсиопендатабасемодекреатедирект) или Direct (msiOpenDatabaseModeDirect) режим. После внесения изменений всегда вызывайте метод [**commit**](database-commit.md) перед закрытием маркера базы данных. Метод **commit** очищает все буферы.

Всегда вызывайте метод [**commit**](database-commit.md) для базы данных, которая была открыта в прямом режиме (Мсиопендатабасемодедирект или мсиопендатабасемодекреатедирект) перед закрытием базы данных. Невозможность сделать это может повредить базу данных.

Поскольку метод **опендатабасе** инициирует доступ к базе данных, он не может использоваться с выполняющейся установкой.

В случае сбоя метода можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




