---
title: Установка параметров ввода
description: Установка параметров ввода
ms.assetid: 288801a7-793f-43bd-9c5a-f9e1bd86ecc3
keywords:
- Расширенный формат систем (ASF), параметры ввода
- ASF (Расширенный системный формат), параметры ввода
- профили, параметры ввода
- кодеки, параметры ввода
- потоки, параметры ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e7b2db64a7346cc8b9d46c48f0add79dafcac95
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103987205"
---
# <a name="to-set-input-settings"></a>Установка параметров ввода

Основные свойства входного носителя и потока мультимедиа определяются структурой [**типа WM \_ Media \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) . Для входных форматов данные типа мультимедиа задаются приложением. Для форматов потока сведения о типе мультимедиа задаются в профиле, который назначается модулю записи. Некоторые свойства не зависят от типа мультимедиа и должны быть заданы для входных данных перед началом записи. Эти свойства являются компонентами кодека и модуля записи, которые не зависят от типа потока, и должны быть заданы после назначения профиля в модуле записи, но перед началом записи.

Для установки входного параметра требуется вызов [**IWMWriterAdvanced2:: сетинпутсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting). Можно также проверить текущее значение параметра с помощью вызова [**IWMWriterAdvanced2:: жетинпутсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Использование профилей с модулем записи**](to-use-profiles-with-the-writer.md)
</dt> <dt>

[**Запись файлов ASF**](writing-asf-files.md)
</dt> <dt>

[**Запись потоков изображений**](writing-image-streams.md)
</dt> </dl>

 

 




