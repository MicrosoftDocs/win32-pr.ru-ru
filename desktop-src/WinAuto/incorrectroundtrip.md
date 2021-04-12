---
title: инкорректраундтрип
description: инкорректраундтрип
ms.assetid: 244537EB-E7DC-49E4-BEAF-CFE3ED25E0B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1f154c0ccc0fff9bb654b94ef9d0807aa459d4b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258786"
---
# <a name="incorrectroundtrip"></a>инкорректраундтрип

## <a name="text"></a>Текст

Вызовите Аккнавигате ((щелкните отложить, чтобы напоминание снова в:), 1, НАВДИР \_ Далее), затем аккнавигате ((Open), 2, навдир \_ Previous), а затем нажмите кнопку отложить, чтобы напоминание снова в: (чилдид = 1), но возвращено нажмите кнопку отложить, чтобы снова выдавать напоминания в:

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

использование [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) для прохода по дереву элементов целевого объекта проверки не возвращает тот же начальный элемент, когда направление обхода отменено.

![Пример недопустимой реализации MSAA, которая привела к неправильной навигации по кругу](images/accchecker-invalid-round-trip.png)

Эта проблема может вызвать проблемы с навигацией для автоматизированных средств, так как обходные элементы могут быть неустойчивыми и непредсказуемыми.

## <a name="possible-causes"></a>Возможные причины

Неправильная или недопустимая реализация MSAA.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**IAccessible:: Аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




