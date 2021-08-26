---
description: Подразделы, содержащиеся в этом разделе, содержат справочные спецификации для интерфейсов для показа рукописных данных.
ms.assetid: 68172566-586C-41AC-82B8-5DBE8B50EC8F
title: Интерфейсы выступающих чернил
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 0c1fb4cab0b8387dec7c75087a72719f72fbc85dc2776a5e20fc6d638fb02d95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092394"
---
# <a name="ink-presenter-interfaces"></a>Интерфейсы выступающих чернил

Подразделы, содержащиеся в этом разделе, содержат справочные спецификации для интерфейсов для [показа рукописных данных](ink-presenter.md) .

## <a name="in-this-section"></a>В этом разделе

| Раздел | Описание |
|---|---|
| [**иинккоммитрекуессандлер**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkcommitrequesthandler)<br/> | Позволяет приложению (вместо объекта [**иинкпресентердесктоп**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) ) фиксировать все ожидающие команды Microsoft DirectComposition в визуальном дереве [DirectComposition](../directcomp/directcomposition-portal.md) приложения.<br/>   |
| [**иинкдесктофост**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost)<br/>                   | Обеспечивает рукописный ввод, обработку и отрисовку с помощью создания потока приложения для размещения объекта [**иинкпресентердесктоп**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) и вставки его в визуальное дерево [DirectComposition](../directcomp/directcomposition-portal.md) приложения. <br/> |
| [**иинкхостворкитем**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkhostworkitem)<br/>                 | Представляет операцию рукописного ввода для выполнения в потоке объекта [**иинкдесктофост**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) .<br/>                                                                                                                                                  |
| [**иинкпресентердесктоп**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop)<br/>         | представляет элемент управления [**InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) , который можно настроить и вставить в визуальное дерево [DirectComposition](../directcomp/directcomposition-portal.md) классического Windows приложения. <br/>                                        |

## <a name="related-topics"></a>Связанные темы

Взаимодействие [рукописного ввода](ink-presenter.md), [перо и](/windows/uwp/design/input/pen-and-stylus-interactions)перо, [Пример анализа рукописного текста](/samples/microsoft/windows-universal-samples/inkanalysis/), [простой пример](/samples/microsoft/windows-universal-samples/simpleink/)с рукописным вводом, [сложный образец для рукописного](/samples/microsoft/windows-universal-samples/complexink/) ввода
