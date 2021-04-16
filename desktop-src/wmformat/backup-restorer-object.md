---
title: Объект резервного хранилища архивации
description: Объект резервного хранилища архивации
ms.assetid: 83ce28c0-fd17-46ff-94c0-d28124a0e56a
keywords:
- Windows Media Format SDK, объекты резервного копирования
- Расширенный формат систем (ASF), объекты резервного копирования
- ASF (Расширенный системный формат), объекты восстановления резервных копий
- объекты, объекты резервного хранилища
- Резервное хранилище архивации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d08e8bec9bb7bbc2a45fbf632e69d230a2536633
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105672249"
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



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Резервное копирование и восстановление лицензий**](backing-up-and-restoring-licenses.md)
</dt> <dt>

[**Объекты**](objects.md)
</dt> </dl>

 

 




