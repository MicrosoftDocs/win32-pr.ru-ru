---
description: Подразделы, содержащиеся в этом разделе, содержат справочные спецификации для интерфейсов для показа рукописных данных.
ms.assetid: 68172566-586C-41AC-82B8-5DBE8B50EC8F
title: Интерфейсы выступающих чернил
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 1839c8ebc0a7597ab7c5becaf7c7492128b4d6af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719483"
---
# <a name="ink-presenter-interfaces"></a>Интерфейсы выступающих чернил

Подразделы, содержащиеся в этом разделе, содержат справочные спецификации для интерфейсов для [показа рукописных данных](ink-presenter.md) .

## <a name="in-this-section"></a>В этом разделе

| Раздел | Описание |
|---|---|
| [**иинккоммитрекуессандлер**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkcommitrequesthandler)<br/> | Позволяет приложению (вместо объекта [**иинкпресентердесктоп**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) ) фиксировать все ожидающие команды Microsoft DirectComposition в визуальном дереве [DirectComposition](../directcomp/directcomposition-portal.md) приложения.<br/>   |
| [**иинкдесктофост**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost)<br/>                   | Обеспечивает рукописный ввод, обработку и отрисовку с помощью создания потока приложения для размещения объекта [**иинкпресентердесктоп**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) и вставки его в визуальное дерево [DirectComposition](../directcomp/directcomposition-portal.md) приложения. <br/> |
| [**иинкхостворкитем**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkhostworkitem)<br/>                 | Представляет операцию рукописного ввода для выполнения в потоке объекта [**иинкдесктофост**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) .<br/>                                                                                                                                                  |
| [**иинкпресентердесктоп**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop)<br/>         | Представляет элемент управления [**InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) , который можно настроить и вставить в визуальное дерево [DirectComposition](../directcomp/directcomposition-portal.md) классического приложения Windows. <br/>                                        |

## <a name="related-topics"></a>См. также

Взаимодействие [рукописного ввода](ink-presenter.md), [перо и](/windows/uwp/design/input/pen-and-stylus-interactions)перо, [Пример анализа рукописного текста](/samples/microsoft/windows-universal-samples/inkanalysis/), [простой пример](/samples/microsoft/windows-universal-samples/simpleink/)с рукописным вводом, [сложный образец для рукописного](/samples/microsoft/windows-universal-samples/complexink/) ввода
