---
description: Чтобы приложение работало с диспетчером синхронизации, необходимо реализовать объект модели COM для управления уведомлениями синхронизации, получаемыми от Синкмгр.
title: Использование диспетчера синхронизации из программы
ms.topic: article
ms.date: 05/31/2018
ms.assetid: bf18d493-0fe7-46e7-9686-f7ee75b3039b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 11e959399624d30e1e6d7ce87fb8bb247de7c9c420ef9b2427c7b9bdeb00e7f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709384"
---
# <a name="using-synchronization-manager-from-a-program"></a>Использование диспетчера синхронизации из программы

Чтобы приложение работало с диспетчером синхронизации, необходимо реализовать объект модели COM для управления уведомлениями синхронизации, получаемыми от Синкмгр. Обработчик приложения выполняет синхронизацию для обрабатываемых элементов. Включается в обработчик, поэтому необходимо реализовать интерфейс [**исинкмгрсинчронизе**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) . Кроме того, необходимо предоставить объект перечислителя и [**исинкмгренумитемс**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) для всех отдельных элементов, которые может синхронизировать приложение.

Синкмгр реализует [**исинкмгрсинчронизекаллбакк**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) и [**исинкмгрсинчронизеинвоке**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronizeinvoke).

Синкмгр вызывает методы в [**исинкмгрсинчронизе**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) для получения информации о элементах, обрабатываемых приложением, и о обработчике, который вы предоставляете для синхронизации этих элементов.

Во время выполнения процесс синхронизации выполняется следующим образом.

1.  Синкмгр уведомляет ваше приложение о том, что время синхронизации происходит для одного из элементов, обрабатываемых приложением путем вызова метода [**исинкмгрсинчронизе:: Initialize**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-initialize) .
2.  Синкмгр вызывает [**исинкмгрсинчронизе:: енумсинкмгритемс**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-enumsyncmgritems) , чтобы получить интерфейс [**исинкмгренумитемс**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) для элементов, обрабатываемых приложением.
3.  Синкмгр вызывает [**исинкмгрсинчронизе:: сетпрогресскаллбакк**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-setprogresscallback) , чтобы предоставить обработчику указатель интерфейса для интерфейса [**исинкмгрсинчронизекаллбакк**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) . Обработчик использует этот интерфейс для обратного вызова Синкмгр во время синхронизации.
4.  Затем Синкмгр вызывает метод [**исинкмгрсинчронизе::P репарефорсинк**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync) , чтобы дать обработчику возможность отобразить любой элемент пользовательского интерфейса, который необходим перед началом синхронизации. Например, в приложении электронной почты может отображаться диалоговое окно входа пользователя.
5.  Обработчик вызывает [**исинкмгрсинчронизекаллбакк:: енаблемоделесс**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-enablemodeless) до и после отображения любых элементов пользовательского интерфейса. По завершении обработчик вызывает [**исинкмгрсинчронизекаллбакк::P репарефорсинккомплетед**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-prepareforsynccompleted) .
6.  Синкмгр вызывает метод [**исинкмгрсинчронизе:: Synchronize**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-synchronize) для запуска синхронизации.

Во время процесса синхронизации Синкмгр будет вызывать методы в интерфейсе [**исинкмгрсинчронизе**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) . Он может отправлять ошибки обработчика, ход выполнения и уведомления. Он также может перечислять элементы, обрабатываемые приложением, или разрешать приложению отображать свойства элементов.

Обработчик вызывает методы в [**исинкмгрсинчронизекаллбакк**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) , чтобы определить, следует ли пропускать элемент, записывать ошибки и отправлять сведения о ходе выполнения в процессе синхронизации.

Дополнительные сведения см. в соответствующих справочных страницах по используемым интерфейсам.

По завершении синхронизации обработчик вызывает [**исинкмгрсинчронизекаллбакк:: синчронизекомплетед**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-synchronizecompleted).

 

 



