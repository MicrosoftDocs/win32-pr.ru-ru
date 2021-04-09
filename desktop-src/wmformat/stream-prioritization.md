---
title: Определение приоритетов потоков
description: Определение приоритетов потоков
ms.assetid: 6b3e9b03-62ef-422b-97ab-197d1cd15beb
keywords:
- Windows Media Format SDK, определение приоритетов потоков
- Расширенный системный формат (ASF), определение приоритетов потоков
- ASF (Расширенный системный формат), определение приоритетов потоков
- Пакет SDK Windows Media Format, порядок приоритетов для потоков
- Расширенный системный формат (ASF), порядок приоритета для потоков
- ASF (Расширенный системный формат), порядок приоритета для потоков
- потоки, определение приоритетов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1628ef050d393cd2d98e73708d5a9ad6c3be4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069584"
---
# <a name="stream-prioritization"></a>Определение приоритетов потоков

При создании файла ASF можно указать порядок приоритета для его составных потоков. Если вы выполняете потоковую передачу по приоритетному файлу и доступная пропускная способность не достаточна для доставки всех потоков, модуль чтения удалит потоки в порядке, соответствующем обратным приоритетам. Таким образом можно гарантировать, что наиболее важные потоки в файле не будут удалены из-за сетевых проблем.

Определение приоритетов потоков настраивается с помощью объекта определения приоритетов потоков и добавляется в профиль. Профиль может содержать только один объект определения приоритетов потоков.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Функции файлов ASF**](asf-file-features.md)
</dt> <dt>

[**IWMProfile3:: Креатеневстреамприоритизатион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)
</dt> <dt>

[**IWMProfile3:: Жетстреамприоритизатион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)
</dt> <dt>

[**IWMProfile3:: Ремовестреамприоритизатион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-removestreamprioritization)
</dt> <dt>

[**IWMProfile3:: Сетстреамприоритизатион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization)
</dt> <dt>

[**Интерфейс Ивмстреамприоритизатион**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization)
</dt> <dt>

[**Использование определения приоритетов потоков**](using-stream-prioritization.md)
</dt> </dl>

 

 




