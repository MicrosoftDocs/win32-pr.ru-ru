---
description: Функция Ексклудеупдатергн исключает область обновления из области обрезки для контекста устройства дисплея.
ms.assetid: e652122b-a3b7-4d1b-8afd-9648d5ee3d42
title: Исключение региона обновления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7be39b948e61fc06c7f7005d15c1163cef0068f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080498"
---
# <a name="excluding-the-update-region"></a>Исключение региона обновления

Функция [**ексклудеупдатергн**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn) исключает область обновления из области обрезки для контекста устройства дисплея. Эта функция полезна при рисовании в окне, отличном от, когда \_ обрабатывается сообщение WM Paint. Он не позволяет рисовать в областях, которые будут обновляться во время следующего \_ сообщения WM Paint.

 

 



