---
title: Реализация собственного Active Accessibility
description: Говорят, что элементы пользовательского интерфейса, реализующие интерфейс IAccessible, предоставляют собственную реализацию.
ms.assetid: 36a5c0cd-53f0-433e-8932-da7d1de177dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4414fa1cd40b66b0971d7c74f484b90c62f86db64722abaabc0e8eea60b14fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859934"
---
# <a name="native-active-accessibility-implementation"></a>Реализация собственного Active Accessibility

Говорят, что элементы пользовательского интерфейса, реализующие интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , предоставляют *собственную реализацию*. Несмотря на то, что затраты на разработку для реализации **IAccessible** (или любого другого интерфейса COM) могут быть высокими, преимущество является исчерпывающим элементом управления информацией, предоставляемой клиентам.

Если приложение использует настраиваемые элементы управления или другие элементы управления, которые не могут быть переданы с помощью Oleacc.dll, необходимо предоставить собственную реализацию.

 

 




