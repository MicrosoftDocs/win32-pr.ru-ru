---
description: Таблица ModuleSignature содержит все сведения, необходимые для обнаружения модуля слияния.
ms.assetid: 5f0b4590-dac3-4528-b714-ff760ae8d123
title: Создание таблиц ModuleSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796775b0237c17db4fa21075a792c372bed3e97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650723"
---
# <a name="authoring-modulesignature-tables"></a>Создание таблиц ModuleSignature

[Таблица ModuleSignature](modulesignature-table.md) содержит все сведения, необходимые для обнаружения модуля слияния.

Поле ModuleID является первичным ключом для этой таблицы и должно соответствовать соглашению, описанному в разделе [именование первичных ключей в базах данных модулей слияния](naming-primary-keys-in-merge-module-databases.md). Например, если понятное имя модуля слияния — MyLibrary, а GUID для модуля слияния — {880DE2F0-CDD8-11D1-A849-006097ABDE17}, то запись в столбце ModuleID таблицы ModuleSignature становится MyLibrary. 880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.

Введите Десятичный идентификатор для языка по умолчанию модуля слияния в поле Language таблицы ModuleSignature.

Введите версию модуля слияния в поле версия.

 

 



