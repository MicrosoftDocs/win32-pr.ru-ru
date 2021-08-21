---
title: Реализация других функций
description: Реализация других функций
ms.assetid: 274ba948-b954-4e9e-a384-dee5b3befbcb
keywords:
- визуализации, интерфейс Ивмпеффектс
- Пользовательские визуализации, интерфейс Ивмпеффектс
- визуализации, функция Render
- Пользовательские визуализации, функция Render
- Функция Render, дополнительные функции
- Интерфейс Ивмпеффектс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73392204357ec856c5c04f2a0f24028ea29e5f09c3aa203d95ed8e2cc7e4ded3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508934"
---
# <a name="implementing-other-functions"></a>Реализация других функций

В определенном случае необходимо написать собственную реализацию функции **Render** . Предоставляются некоторые другие функции, которые также являются функциями членов интерфейса **ивмпеффектс** . некоторые будут предоставлять дополнительные сведения, которые можно использовать, а другие будут автоматически предоставлять проигрыватель Windows Media с информацией, созданной мастером, например именем визуализации.

Интерфейс **ивмпеффектс** поддерживает следующие функции в дополнение к **визуализации**:



| Функция                                                   | Описание                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [дисплайпропертипаже](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-displaypropertypage) | Реализация по умолчанию, не предоставляемая мастером.                                                                                                                                                                                                                                                           |
| [GetCapabilities](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getcapabilities)         | возвращает возможности визуализации и передает их в проигрыватель Windows Media.                                                                                                                                                                                                                     |
| [жеткуррентпресет](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getcurrentpreset)       | Мастер создал две предустановки при создании кода для визуализации. Эта функция вызывается, когда разработчику обложки требуется получить индекс текущей предустановки. Вы не хотите изменять реализацию этой функции, так как она просто использует сведения, заданные другими функциями. |
| [жетпресеткаунт](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getpresetcount)           | Мастер создал две предустановки при создании кода для визуализации. Вы можете изменить счетчик, изменив реализацию **жетпресеткаунт**. Дополнительные сведения об изменении предустановок см. в разделе [предустановки](presets.md) .                                                             |
| [жетпресеттитле](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getpresettitle)           | Мастер создал две предустановки при создании кода для визуализации. Можно изменить заголовки, используемые при изменении реализации **жетпресеттитле**. Дополнительные сведения об изменении предустановок см. в разделе [предустановки](presets.md) .                                                       |
| [GetTitle](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-gettitle)                       | возвращает заголовок визуализации и передает его в проигрыватель Windows Media. Мастер использовал имя проекта для создания имени, которое передается обратно.                                                                                                                                           |
| [гофуллскрин](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-gofullscreen)               | Реализация по умолчанию, не предоставляемая мастером.                                                                                                                                                                                                                                                           |
| [Файла MediaInfo](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-mediainfo)                     | Извлекает количество звуковых каналов и частоту выборки звука, воспроизводимой в текущий момент.                                                                                                                                                                                                               |
| [рендерфуллскрин](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-renderfullscreen)       | Реализация по умолчанию, не предоставляемая мастером.                                                                                                                                                                                                                                                           |
| [сеткуррентпресет](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-setcurrentpreset)       | Мастер создал две предустановки при создании кода для визуализации. эта функция вызывается, когда проигрыватель Windows Media хочет перейти на именованную предустановку.                                                                                                                                   |



 

Интерфейс **IWMPEffects2** поддерживает следующие дополнительные функции:



| Функция                                            | Описание                                                                                                                                      |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Создание](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create)                   | при подготовке к просмотру в окне проигрыватель Windows Media вызывает эту функцию, чтобы можно было создать новое окно для отрисовки.                          |
| [Завершить](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-destroy)                 | при отрисовке в окне проигрыватель Windows Media вызывает эту функцию, чтобы можно было уничтожить окно, созданное при вызове метода **Create** . |
| [нотифиневмедиа](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-notifynewmedia)   | Эта функция позволяет визуализации реагировать при загрузке проигрывателем нового элемента мультимедиа.                                          |
| [онвиндовмессаже](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-onwindowmessage) | Эта функция получает сообщения Windows от проигрывателя при отрисовке в режиме без окон.                                                       |
| [рендервиндовед](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-renderwindowed)   | Эта функция вызывается проигрывателем вместо **ивмпеффектс:: Render, когда проигрыватель подготавливается** к просмотру в оконном режиме.                          |
| [сеткоре](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-setcore)                 | Эта функция получает указатель на интерфейс **ивмпкоре** .                                                                                  |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Реализация кода**](implementing-your-code.md)
</dt> </dl>

 

 




