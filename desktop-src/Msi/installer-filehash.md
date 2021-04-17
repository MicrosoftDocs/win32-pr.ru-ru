---
description: Метод FileHash объекта Installer принимает путь к файлу и возвращает 128-разрядный хэш этого файла. Сведения о хэш-файле возвращаются в виде объекта записи. Весь 128-разрядный хэш-файл возвращается в виде полей свойств 4 32-bit IntegerData.
ms.assetid: 065ffde1-4d7c-4e71-9315-7926d4cd38ed
title: Метод Installer. FileHash
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileHash
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a38ef741c5c3a33c526cc78fbdc4551716ed3ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651608"
---
# <a name="installerfilehash-method"></a>Метод Installer. FileHash

Метод **FileHash** [**объекта Installer**](installer-object.md) принимает путь к файлу и возвращает 128-разрядный хэш этого файла. Сведения о хэш-файле возвращаются в виде [**объекта записи**](record-object.md). Весь 128-разрядный хэш-файл возвращается в виде полей свойств 4 32-bit [**IntegerData**](record-integerdata.md) .

Значения, возвращаемые в [**объекте Record**](record-object.md) , соответствуют четырем полям структуры [**мсифилехашинфо**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo) , возвращаемой [**мсижетфилехаш**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha). Нумерация четырех полей составляет 1 на основе [таблицы мсифилехаш](msifilehash-table.md).

-   Поле 1 соответствует столбцу HashPart1.
-   Поле 2 соответствует столбцу HashPart2.
-   Поле 3 соответствует столбцу HashPart3.
-   Поле 4 соответствует столбцу HashPart4.

## <a name="syntax"></a>Синтаксис


```JScript
Installer.FileHash(
  FilePath,
  Options
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Равно* 
</dt> <dd>

Путь к файлу, который необходимо хэшировать.

</dd> <dt>

*Параметры* 
</dt> <dd>

Зарезервировано для последующего использования.

Значение этого параметра должно быть равно 0 (нулю).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успешного выполнения этот метод возвращает [**объект Record**](record-object.md) , содержащий хэш файла.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Управление версиями файлов по умолчанию](default-file-versioning.md)
</dt> <dt>

[Управление размерами и версиями файлов](manage-file-sizes-and-versions.md)
</dt> <dt>

[Таблица Мсифилехаш](msifilehash-table.md)
</dt> <dt>

[**мсижетфилехаш**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> </dl>

 

 




