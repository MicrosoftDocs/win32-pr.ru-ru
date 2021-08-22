---
title: Рендеринг изображений
description: Рендеринг изображений
ms.assetid: de87f288-f1bd-471c-b594-e9dbde3cff0a
keywords:
- Дравдиб, отрисовка изображения
- Дравдиб, рисование DIB
- Функция Дравдибдрав
- Функция Дравдибжетбуффер
- Функция Дравдибупдате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7be73fbe37a28ab44116d2fb2e68acb6a9a3a385603af23dca0e14aa2de4d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690754"
---
# <a name="image-rendering"></a>Рендеринг изображений

После вызова [**дравдибопен**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) для создания дравдиб DC (см. [дравдиб Operations](drawdib-operations.md)) можно нарисовать изображение DIB на экране с помощью функции [**дравдибдрав**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) . **Дравдибдрав** отменяет цветные точечные рисунки при отображении их с помощью 8-разрядных видеоадаптеров.

[**Дравдибдрав**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) также поддерживает прозрачное воспроизведение видео при отображении сжатых растровых изображений. Доступ к буферу, содержащему распакованное изображение, можно получить с помощью функции [**дравдибжетбуффер**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) . **Дравдибжетбуффер** возвращает **значение NULL** при прорисовке несжатого точечного рисунка. Необходимо подготовить приложение к обработке сжатых и несжатых точечных рисунков.

Вы можете обновить изображение или часть изображения, отображаемого приложением, с помощью макроса [**дравдибупдате**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[О функциях Дравдиб](about-the-drawdib-functions.md)
</dt> </dl>

 

 




