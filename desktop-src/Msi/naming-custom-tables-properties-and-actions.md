---
description: Авторы пакетов должны гарантировать, что имена любых настраиваемых таблиц, свойств или действий, определенных в их пакете, не будут конфликтовать с именами стандартных таблиц, свойств или действий, которые являются собственными для установщик Windows.
ms.assetid: f86b51c5-161a-4218-987d-f17116e4f668
title: Именование настраиваемых таблиц, свойств и действий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aabd35fb1456f6aefbd05d486b1d86420bf5013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898850"
---
# <a name="naming-custom-tables-properties-and-actions"></a><span data-ttu-id="28f9a-103">Именование настраиваемых таблиц, свойств и действий</span><span class="sxs-lookup"><span data-stu-id="28f9a-103">Naming Custom Tables, Properties, and Actions</span></span>

<span data-ttu-id="28f9a-104">Авторы пакетов должны гарантировать, что имена любых настраиваемых таблиц, свойств или действий, определенных в их пакете, не будут конфликтовать с именами стандартных таблиц, свойств или действий, которые являются собственными для установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="28f9a-104">Package authors should ensure that the names of any custom tables, properties, or actions defined in their package will not conflict with the names of standard tables, properties, or actions that are native to the Windows Installer.</span></span>

<span data-ttu-id="28f9a-105">Авторы пакетов должны следовать следующим правилам для настраиваемых имен таблиц, свойств и действий.</span><span class="sxs-lookup"><span data-stu-id="28f9a-105">Package authors should adhere to the following guidelines for custom table, property, or action names.</span></span>

-   <span data-ttu-id="28f9a-106">Создание имен для пользовательских таблиц, свойств или действий с префиксом, идентифицирующим приложение.</span><span class="sxs-lookup"><span data-stu-id="28f9a-106">Make names for custom tables, properties, or actions that have a prefix that identifies your application.</span></span>
-   <span data-ttu-id="28f9a-107">Никогда не используйте имя с MSI в качестве префикса.</span><span class="sxs-lookup"><span data-stu-id="28f9a-107">Never use a name with Msi as the prefix.</span></span> <span data-ttu-id="28f9a-108">Начиная с установщик Windows 2,0, всем новым свойствам, действиям и таблицам в машинном установщик Windows присваиваются имена с префиксом MSI.</span><span class="sxs-lookup"><span data-stu-id="28f9a-108">Starting with Windows Installer 2.0, all new native Windows Installer properties, actions, and tables are given names prefixed by Msi.</span></span> <span data-ttu-id="28f9a-109">Этот префикс не чувствителен к регистру, например Мсиневинтерналтабле.</span><span class="sxs-lookup"><span data-stu-id="28f9a-109">This prefix is not case sensitive, for example MsiNewInternalTable.</span></span> <span data-ttu-id="28f9a-110">Поскольку префикс не чувствителен к регистру, авторы должны избегать всех вариантов префикса MSI.</span><span class="sxs-lookup"><span data-stu-id="28f9a-110">Because the prefix is not case sensitive, authors should avoid all cases of the Msi prefix.</span></span>

<span data-ttu-id="28f9a-111">Дополнительные сведения см. в разделе [имена таблиц](table-names.md).</span><span class="sxs-lookup"><span data-stu-id="28f9a-111">For more information, see [Table Names](table-names.md).</span></span>

 

 



