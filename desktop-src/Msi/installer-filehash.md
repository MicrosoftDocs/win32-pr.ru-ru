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
ms.openlocfilehash: a2da76ef3f0606002e26e8c320f83ca45e46bbbeb573d509c235c9fca8932247
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630795"
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
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
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

 

 




