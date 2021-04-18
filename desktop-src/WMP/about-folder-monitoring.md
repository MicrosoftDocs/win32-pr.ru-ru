---
title: О мониторинге папок
description: О мониторинге папок
ms.assetid: d3d83e60-ecc7-4501-a6dd-15f7680a6ec9
keywords:
- Проигрыватель Windows Media, мониторинг папок
- Объектная модель проигрывателя Windows Media, мониторинг папок
- Объектная модель, мониторинг папок
- Элемент управления ActiveX проигрывателя Windows Media, мониторинг папок
- Элемент управления ActiveX, мониторинг папок
- Элемент управления ActiveX мобильных устройств проигрывателя Windows Media, мониторинг папок
- Проигрыватель Windows Media Mobile, мониторинг папок
- мониторинг папок
- мониторинг папок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3d6af341df706cd85c4158197b27babad09c86
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412474"
---
# <a name="about-folder-monitoring"></a>О мониторинге папок

Проигрыватель Windows Media может отслеживать папки, содержащие цифровые файлы мультимедиа, и обновлять библиотеку при добавлении или удалении файлов. Эта функция мониторинга папок обеспечивается интерфейсом [ивмпфолдермониторсервицес](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices) .

Чтобы использовать службы наблюдения за папками, необходимо создать объект Player в удаленном состоянии. Дополнительные сведения об удаленном взаимодействии см. [в разделе Удаленное взаимодействие с элементом управления проигрывателя Windows Media](remoting-the-windows-media-player-control.md). После создания удаленного экземпляра проигрывателя получите указатель на интерфейс **ивмпфолдермониторсервицес** , вызвав **QueryInterface** в интерфейсе [ивмпплайер](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) .

Проигрыватель Windows Media хранит список отслеживаемых папок. Чтобы получить список наблюдаемых папок, используйте методы [ивмпфолдермониторсервицес:: Get \_ Count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) и [ивмпфолдермониторсервицес:: Item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) . Чтобы добавить папки в список или удалить их из списка, используйте методы [ивмпфолдермониторсервицес:: Add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) и [Remove](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove) соответственно.

**Запуск проверки**

Наблюдение за папками обычно является фоновым процессом, который не требуется вызывать явным образом. Если вы хотите активно сканировать папку, вызовите [ивмпфолдермониторсервицес:: стартскан](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan). Вы можете прерывать выполнение проверки с помощью метода [ивмпфолдермониторсервицес:: стопскан](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan) .

**Получение состояния мониторинга папки**

**Ивмпфолдермониторсервицес** предоставляет функциональные возможности для получения состояния процесса наблюдения за папками.

Сканирование папок выполняется в два прохода. При первом прохождении проигрыватель сканирует папки, имена которых находятся в списке наблюдаемых папок, по одному и создает список файлов, которые будут добавлены в библиотеку. Во втором прохождении он просматривает список файлов и добавляет файлы в библиотеку, а также удаляет все элементы мультимедиа из библиотеки, соответствующие физические файлы которой были удалены из файловой системы.

Событие [фолдерсканстатечанже](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange) используется для уведомления программы при каждом переключении проигрывателя на новое состояние. Можно также получить текущее состояние, вызвав [Get \_ scanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate). При запуске первого прохода текущее значение состояния — Вмпфсссканнинг. Во время второго прохода состояние переключается на Вмпфссупдатинг. После завершения процесса состояние изменится на Вмпфссстоппед.

Пока проигрыватель сканирует отслеживаемые папки на первом этапе, вызовите [Get \_ сканнедфилескаунт](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) , чтобы проверить количество проверенных файлов. Метод [Get \_ куррентфолдер](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder) будет указывать, в какой папке в данный момент выполняется сканирование.

После запуска второго прохода вызовите [Get \_ аддедфилескаунт](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) , чтобы проверить, сколько файлов было добавлено в библиотеку. Метод [Get \_ updateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress) сообщит о ходе выполнения второго прохода в процентах от 0 до 100.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Сведения об объектной модели проигрывателя**](about-the-player-object-model.md)
</dt> <dt>

[**Интерфейс Ивмпфолдермониторсервицес**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
</dt> </dl>

 

 




