---
title: Сохранение содержимого
description: Сохранение содержимого
ms.assetid: 22f4e580-43a4-48b5-8eb3-90e1346a1093
keywords:
- Windows Media Format SDK, сохранение содержимого
- Windows Media Format SDK, Быстрая потоковая передача кэша
- Расширенный формат систем (ASF), сохранение содержимого
- ASF (Расширенный системный формат), сохранение содержимого
- Расширенный системный формат (ASF), Быстрая потоковая передача кэша
- ASF (Расширенный системный формат), Быстрая потоковая передача кэша
- потоки, сохранение содержимого
- Быстрая потоковая передача кэша, сохранение содержимого
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6c215a81accef29f8943ed52ca24264f785d94
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789210"
---
# <a name="saving-content"></a>Сохранение содержимого

С помощью этого пакета SDK приложение может сохранить загруженное или потоковое содержимое на локальном компьютере пользователя, вызвав метод [**IWMReaderAdvanced2:: SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) для объекта Reader. Для потокового содержимого сервер должен использовать быструю потоковую передачу кэша, как описано в разделе [Включение быстрой потоковой передачи кэша от клиента](enabling-fast-cache-streaming-from-the-client.md). Для потокового содержимого метод **SaveFileAs** создает ASX файл, указывающий на ASF файл, содержащий сохраненное содержимое. Если объект модуля чтения потоковой передачи списка воспроизведения на стороне сервера, каждая запись сохраняется в виде отдельного ASF-файла, а файл ASX указывает на каждый из файлов ASF. Для загруженного содержимого метод **SaveFileAs** просто создает файл ASF.

Чтобы сохранить содержимое в локальном файле, выполните следующие действия.

1.  Вызовите [**ивмреадер:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) с URL-адресом. **Open** является асинхронным вызовом и возвращается немедленно. Дождитесь завершения операции, как описано в разделе [Создание читателя и открытие файла](to-create-a-reader-and-open-a-file.md).
2.  Запросите объект модуля чтения для интерфейса [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) .
3.  Проверьте, можно ли сохранить содержимое, вызвав метод [**IWMReaderAdvanced4:: кансавефилеас**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cansavefileas) . Если метод возвращает значение false, содержимое не может быть сохранено локально. В противном случае перейдите к шагу 4.
4.  Вызовите метод [**IWMReaderAdvanced4:: исусингфасткаче**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-isusingfastcache) , чтобы определить, использует ли сервер быструю потоковую передачу кэша.
5.  Вызовите [**IWMReaderAdvanced2:: SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) с именем файла для локального файла. Если метод **исусингфасткаче** возвращает значение true, присвойте файлу расширение ASX. В противном случае укажите имя файла с расширением ASF, WMA или WMV.

Приложение может отменить операцию сохранения во время выполнения, вызвав метод [**IWMReaderAdvanced4:: канцелсавефилеас**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cancelsavefileas) .

Сохраненное содержимое может быть защищено с помощью DRM, поэтому может оказаться невозможным воспроизведение файла на другом компьютере. Дополнительные сведения о защите содержимого см. в статье [функции цифрового Rights Management](digital-rights-management-features.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ивмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Интерфейс IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




