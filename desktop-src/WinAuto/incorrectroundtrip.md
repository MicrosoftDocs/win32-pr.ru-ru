---
title: инкорректраундтрип
description: инкорректраундтрип
ms.assetid: 244537EB-E7DC-49E4-BEAF-CFE3ED25E0B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17f0ca96496a9e98c1068354e3a9efda27ca8cb0993f6f924ea68ef7d0c1436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644743"
---
# <a name="incorrectroundtrip"></a>инкорректраундтрип

## <a name="text"></a>Текст

Вызовите Аккнавигате ((щелкните отложить, чтобы напоминание снова в:), 1, НАВДИР \_ Далее), затем аккнавигате ((Open), 2, навдир \_ Previous), а затем нажмите кнопку отложить, чтобы напоминание снова в: (чилдид = 1), но возвращено нажмите кнопку отложить, чтобы снова выдавать напоминания в:

## <a name="type"></a>Тип

Error

## <a name="description"></a>Описание

использование [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) для прохода по дереву элементов целевого объекта проверки не возвращает тот же начальный элемент, когда направление обхода отменено.

![Пример недопустимой реализации MSAA, которая привела к неправильной навигации по кругу](images/accchecker-invalid-round-trip.png)

Эта проблема может вызвать проблемы с навигацией для автоматизированных средств, так как обходные элементы могут быть неустойчивыми и непредсказуемыми.

## <a name="possible-causes"></a>Возможные причины

Неправильная или недопустимая реализация MSAA.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**IAccessible:: Аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




