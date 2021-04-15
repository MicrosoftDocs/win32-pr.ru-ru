---
description: Инструментарий WMI в настоящее время не поддерживает управляемый код на WMI, но поддерживается в MI.
ms.assetid: ED6EF216-7FF7-45F2-9FDD-3A73D5F65F9B
ms.tgt_platform: multiple
title: Создание управляемого клиента WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb1339347c4e15cd29ebf4d4e98e5a8b61a24e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702080"
---
# <a name="creating-a-managed-wmi-client"></a>Создание управляемого клиента WMI

Текущий выпуск WMI содержит пространство имен System. Management, которое предоставляет ряд API, взаимодействующих с WMI. Однако использовать это пространство имен не рекомендуется.

Если вы хотите создать управляемый клиент WMI, рекомендуется использовать инфраструктуру управления Windows (MI). MI — это версия WMI следующего поколения, которая содержит полную поддержку управляемого кода. Дополнительные сведения см. [в разделе Реализация управляемого клиента MI](/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client).

 

 
