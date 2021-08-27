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
ms.openlocfilehash: 6f28b01cb3b4506e0b47332cc3336af95dd641e78c7716f33b8e62b162081bdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071524"
---
# <a name="creating-a-managed-wmi-client"></a>Создание управляемого клиента WMI

Текущий выпуск WMI содержит пространство имен System. Management, которое предоставляет ряд API, взаимодействующих с WMI. Однако использовать это пространство имен не рекомендуется.

если вы хотите создать управляемый клиент WMI, рекомендуется использовать инфраструктуру управления Windows (MI). MI — это версия WMI следующего поколения, которая содержит полную поддержку управляемого кода. Дополнительные сведения см. [в разделе Реализация управляемого клиента MI](/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client).

 

 
