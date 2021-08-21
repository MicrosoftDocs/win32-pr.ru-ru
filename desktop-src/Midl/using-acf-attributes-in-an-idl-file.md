---
title: Использование атрибутов ACF в IDL-файле
description: Можно использовать \_ параметр КОМПИЛЯТОРА MIDL/АПП config, чтобы указать атрибуты обработчика привязки в IDL-файле, а не в отдельном файле ACF.
ms.assetid: 3558e818-b39f-42a4-842f-05970296da0e
keywords:
- ACF MIDL, атрибуты, использование ACF в IDL
- IDL-MIDL, использование ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bda925a3b3242072f297c8828427ae4f7a488d1f3b002e05ace6bec45a46d2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105524"
---
# <a name="using-acf-attributes-in-an-idl-file"></a>Использование атрибутов ACF в IDL-файле

Можно использовать параметр компилятора MIDL/[**app \_ config**](-app-config.md) , чтобы указать атрибуты обработчика привязки в IDL-файле, а не в отдельном файле ACF. В частности, к заголовку интерфейса RPC в IDL-файле можно применить [**Автоматические \_ маркеры**](auto-handle.md), [**неявный \_ обработчик**](implicit-handle.md)и [**явные атрибуты \_ обработчиков**](explicit-handle.md) . Рекомендуется использовать этот параметр, если приложению RPC не требуются другие атрибуты ACF, и если не требуется обязательная совместимость с использование-DCE.

 

 




