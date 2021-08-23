---
title: Объект резервного хранилища архивации
description: Объект резервного хранилища архивации
ms.assetid: 83ce28c0-fd17-46ff-94c0-d28124a0e56a
keywords:
- Windows Пакет SDK для формата мультимедиа, объекты резервного хранилища
- Расширенный формат систем (ASF), объекты резервного копирования
- ASF (Расширенный системный формат), объекты восстановления резервных копий
- объекты, объекты резервного хранилища
- Резервное хранилище архивации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a7bf14f8afda284d8d0ae3d4f36d37fff0baa63f4f42802a98830038ec2d850
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028132"
---
# <a name="backup-restorer-object"></a>Объект резервного хранилища архивации

Средство резервного копирования предоставляет интерфейсы для управления резервными копиями лицензий, обычно на съемные носители, а затем восстанавливает их на новый компьютер.

Объект резервного хранилища создается функцией [**вмкреатебаккупресторер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) , которая устанавливает указатель на интерфейс [**ивмлиценсебаккуп**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) . Другие интерфейсы объекта резервного хранилища можно получить, вызвав метод **QueryInterface** .

Объект резервного хранилища поддерживает следующие интерфейсы.



| Интерфейс                                              | Описание                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ивмбаккупресторепропс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops) | Задает и получает свойства, необходимые для интерфейсов [**ивмлиценсебаккуп**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) и [**ивмлиценсересторе**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) . |
| [**ивмлиценсебаккуп**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)           | Резервное копирование лицензий, как правило, для их восстановления на другом компьютере.                                                                          |
| [**ивмлиценсересторе**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)         | Восстанавливает лицензии.                                                                                                                                        |



 

Для использования объекта резервного хранилища в приложении должен быть реализован следующий интерфейс обратного вызова.



| Интерфейс                                      | Описание                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**ивмстатускаллбакк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Получает сообщения о состоянии от процессов, выполняемых в отдельном потоке. |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Резервное копирование и восстановление лицензий**](backing-up-and-restoring-licenses.md)
</dt> <dt>

[**Объекты**](objects.md)
</dt> </dl>

 

 




