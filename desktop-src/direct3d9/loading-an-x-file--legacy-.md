---
description: Для загрузки файла x используйте следующую процедуру в приложениях прежних версий.
ms.assetid: 2b975873-2e5d-4c64-a022-d2098c3d95b8
title: Загрузка файла X (прежних версий) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716ed54afdc7d1aa18fdde992a0799a8990a49c6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537028"
---
# <a name="loading-an-x-file-legacy-direct3d-9"></a>Загрузка файла X (прежних версий) (Direct3D 9)

Для загрузки файла x используйте следующую процедуру в приложениях прежних версий.

1.  Используйте функцию [**директксфилекреате**](directxfilecreate.md) для создания объекта [**идиректксфиле**](idirectxfile.md) .
2.  Если в файле DirectX есть шаблоны, которые будут загружены, используйте метод [**идиректксфиле:: регистертемплатес**](idirectxfile--registertemplates.md) для регистрации этих шаблонов.
3.  Используйте метод [**идиректксфиле:: креатинумобжект**](idirectxfile--createenumobject.md) для создания объекта перечислителя [**идиректксфилинумобжект**](idirectxfileenumobject.md) .
4.  Перебрать объекты в файле. Для каждого объекта выполните следующие действия.
    1.  Используйте метод [**идиректксфилинумобжект:: жетнекстдатаобжект**](idirectxfileenumobject--getnextdataobject.md) для получения каждого объекта [**идиректксфиледата**](idirectxfiledata.md) .
    2.  Используйте метод [**идиректксфиледата:: GetType**](idirectxfiledata--gettype.md) для получения типа данных.
    3.  Загрузите данные с помощью метода [**идиректксфиледата:: GetData**](idirectxfiledata--getdata.md) .
    4.  Если у объекта есть необязательные элементы, извлеките необязательные члены, вызвав метод [**идиректксфиледата:: жетнекстобжект**](idirectxfiledata--getnextobject.md) .
    5.  Освободите объект [**идиректксфиледата**](idirectxfiledata.md) .
5.  Освободите объект [**идиректксфилинумобжект**](idirectxfileenumobject.md) .
6.  Освободите объект [**идиректксфиле**](idirectxfile.md) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[X-файлы (прежние версии)](x-files--legacy-.md)
</dt> </dl>

 

 



