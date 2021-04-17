---
description: 'Расширение оснастки "вложение" не позволяет напрямую запрашивать базу данных безопасности для получения информации. Вместо этого он должен запрашивать эти сведения из оснасток настройки безопасности с помощью Исцесвкаттачментдата:: GetData.'
ms.assetid: 1171beed-5b28-4f31-b33f-533e3c631b0d
title: Получение данных из оснастки конфигурации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c888cef92a354f73f01e87fca12cee2567dab48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546210"
---
# <a name="getting-data-from-the-configuration-snap-ins"></a>Получение данных из оснастки конфигурации

Расширение оснастки "вложение" не позволяет напрямую запрашивать базу данных безопасности для получения информации. Вместо этого он должен запрашивать эти сведения из оснасток настройки безопасности с помощью [**исцесвкаттачментдата:: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).

Оснастка "вложение" может извлекать все данные при инициализации самой себя или получать информацию при открытии его узла.

> [!Note]  
> Необходимо использовать метод [**исцесвкаттачментдата:: фрибуффер**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-freebuffer) , чтобы освободить буфер, выделенный методом оснастки настройки безопасности [**Исцесвкаттачментдата:: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).

 

 

 



