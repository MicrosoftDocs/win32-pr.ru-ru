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
# <a name="authoring-modulesignature-tables"></a><span data-ttu-id="233df-103">Создание таблиц ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="233df-103">Authoring ModuleSignature Tables</span></span>

<span data-ttu-id="233df-104">[Таблица ModuleSignature](modulesignature-table.md) содержит все сведения, необходимые для обнаружения модуля слияния.</span><span class="sxs-lookup"><span data-stu-id="233df-104">The [ModuleSignature table](modulesignature-table.md) contains all the information needed to identify the merge module.</span></span>

<span data-ttu-id="233df-105">Поле ModuleID является первичным ключом для этой таблицы и должно соответствовать соглашению, описанному в разделе [именование первичных ключей в базах данных модулей слияния](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="233df-105">The ModuleID field is the primary key for this table and must follow the convention described in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span> <span data-ttu-id="233df-106">Например, если понятное имя модуля слияния — MyLibrary, а GUID для модуля слияния — {880DE2F0-CDD8-11D1-A849-006097ABDE17}, то запись в столбце ModuleID таблицы ModuleSignature становится MyLibrary. 880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.</span><span class="sxs-lookup"><span data-stu-id="233df-106">For example, if the readable name of the merge module is MyLibrary and the GUID for the merge module is {880DE2F0-CDD8-11D1-A849-006097ABDE17}, the entry in the ModuleID column of the ModuleSignature table becomes MyLibrary.880DE2F0\_CDD8\_11D1\_A849\_006097ABDE17.</span></span>

<span data-ttu-id="233df-107">Введите Десятичный идентификатор для языка по умолчанию модуля слияния в поле Language таблицы ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="233df-107">Enter the decimal identifier for the default language of the merge module into the Language field of the ModuleSignature table.</span></span>

<span data-ttu-id="233df-108">Введите версию модуля слияния в поле версия.</span><span class="sxs-lookup"><span data-stu-id="233df-108">Enter the version of the merge module into the Version field.</span></span>

 

 



