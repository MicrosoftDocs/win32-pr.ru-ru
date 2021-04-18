---
description: Чтобы обеспечить визуальное обновление, приложение должно использовать Идиректманипулатионкомпоситор.
ms.assetid: 6D8FB359-F52B-43F9-8A62-6BB2AEDE4F2B
title: Механизм композиции
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: aa4d922893472c1fe235bae60e41a00924d13bba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494952"
---
# <a name="composition-engine"></a>Механизм композиции

Чтобы обеспечить визуальное обновление, приложение должно использовать [**идиректманипулатионкомпоситор**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor). Этот объект отвечает за обновление визуальных элементов на основе обновлений [непосредственного управления](direct-manipulation-portal.md) , переход на обновления инерции и предоставление сведений о времени компоновки для непосредственной манипуляции. Кроме того, приложение должно использовать [дкомпманипулатионкомпоситор](direct-manipulation-guids.md) , предоставляемый [непосредственной манипуляцией](direct-manipulation-portal.md), который будет обрабатывать все визуальные обновления от имени приложения и управлять обновлениями инерции.

[Дкомпманипулатионкомпоситор](direct-manipulation-guids.md) является реализацией интерфейса [**идиректманипулатионкомпоситор**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) , который заключает [DirectComposition](../directcomp/directcomposition-portal.md). Вместо того, чтобы приложение применяло выходные данные, через [прямую манипуляцию](direct-manipulation-portal.md) с объектом-компоновщиком можно применить выходные данные, установив преобразования непосредственно в дереве DirectComposition. С помощью этой конфигурации можно обрабатывать входные и выходные преобразования, независимо от действий в потоке пользовательского интерфейса.

Чтобы предоставить сведения о [прямой манипуляции](direct-manipulation-portal.md) по времени механизма композиции, класс [Дкомпманипулатионкомпоситор](direct-manipulation-guids.md) реализует интерфейс [**идиректманипулатионфрамеинфопровидер**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationframeinfoprovider) . При создании окна просмотра [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) [**идиректманипулатионкомпоситор**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) указатель, полученный из [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для экземпляра **идиректманипулатионфрамеинфопровидер**. Указатель **идиректманипулатионфрамеинфопровидер** передается в функцию [**Идиректманипулатионманажер:: креатевиевпорт ()**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-createviewport) .
