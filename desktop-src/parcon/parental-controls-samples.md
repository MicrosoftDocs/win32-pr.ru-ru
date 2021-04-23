---
description: Примеры родительского контроля
ms.assetid: 19dac95c-2279-4bf9-a58c-dd30177c0c9d
title: Примеры родительского контроля
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26962f4edd16e1e860883607316d5a7cbf3d9122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693425"
---
# <a name="parental-controls-samples"></a><span data-ttu-id="10286-103">Примеры родительского контроля</span><span class="sxs-lookup"><span data-stu-id="10286-103">Parental Controls Samples</span></span>

<span data-ttu-id="10286-104">Пример кода для родительского контроля доступен по пути <installation directory> \\ Windows \\ <version number> \\ Samples \\ Security \\ паренталконтролс.</span><span class="sxs-lookup"><span data-stu-id="10286-104">Sample code for Parental Controls is available under path <installation directory>\\Windows\\<version number>\\Samples\\Security\\ParentalControls.</span></span> <span data-ttu-id="10286-105">Ниже приведены примеры.</span><span class="sxs-lookup"><span data-stu-id="10286-105">The samples are as follows:</span></span>

## <a name="utilities"></a><span data-ttu-id="10286-106">Служебные программы</span><span class="sxs-lookup"><span data-stu-id="10286-106">Utilities</span></span>

<span data-ttu-id="10286-107">Вспомогательные функции для базового управления COM, строковых операций SID и функций чтения и записи WMI.</span><span class="sxs-lookup"><span data-stu-id="10286-107">Helper functionality for basic COM management, SID string operations, and WMI read and write functionality.</span></span> <span data-ttu-id="10286-108">Все остальные примеры зависят от этого проекта, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="10286-108">All of the other samples depend on this project unless otherwise specified.</span></span>

## <a name="complianceapi"></a><span data-ttu-id="10286-109">комплианцеапи</span><span class="sxs-lookup"><span data-stu-id="10286-109">ComplianceAPI</span></span>

<span data-ttu-id="10286-110">Консольное приложение, управляемое командной строкой, демонстрирует использование API соответствия для получения ключевых подмножеств параметров для пользователя.</span><span class="sxs-lookup"><span data-stu-id="10286-110">Command-line driven console application demonstrating how to use the Compliance API to retrieve a key subset of settings for a user.</span></span>

## <a name="complianceapp"></a><span data-ttu-id="10286-111">комплианцеапп</span><span class="sxs-lookup"><span data-stu-id="10286-111">ComplianceApp</span></span>

<span data-ttu-id="10286-112">Простое консольное приложение, демонстрирующие использование API соответствия для проверки необходимости ведения журнала и конкретных ограничений.</span><span class="sxs-lookup"><span data-stu-id="10286-112">Simple console application demonstrating use of the Compliance API to check for logging required and specific restrictions.</span></span> <span data-ttu-id="10286-113">Если ограничения по времени включены, приложение также ожидает от ожидаемых событий выхода.</span><span class="sxs-lookup"><span data-stu-id="10286-113">If time restrictions are enabled, the application also waits for the impending logout events.</span></span>

## <a name="uiextensibility"></a><span data-ttu-id="10286-114">уиекстенсибилити</span><span class="sxs-lookup"><span data-stu-id="10286-114">UIExtensibility</span></span>

<span data-ttu-id="10286-115">Консольное приложение, управляемое командной строкой, демонстрирующие использование API WMI и схемы WPC для перечисления, запроса, добавления, изменения и удаления записей ссылок на расширяемость пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="10286-115">Command-line driven console application demonstrating use of the WMI APIs and WPC schema to list, query, add, modify, and delete UI Extensibility link entries.</span></span>

<span data-ttu-id="10286-116">Пример командной строки для примера:</span><span class="sxs-lookup"><span data-stu-id="10286-116">Example command line for sample:</span></span>

<span data-ttu-id="10286-117">«D: \\ WPC \\ Samples \\ Security \\ паренталконтролс \\ уиекстенсибилити \\ Debug \\ уиекстенсибилити» Add/g: {FD59BB7F-54AB-11DB-9666-00E08161165F}/c: 0/N: D:/WPC/Samples/Security/паренталконтролс/уиекстрк/Debug/UiExtRC.dll,-101/S: d:/WPC/Samples/Security/паренталконтролс/UiExtRC/Debug/UiExtRC.dll,-103/I: D:/WPC/Samples/Security/ParentalControls/UiExtRC/Debug/UiExtRC.dll,-104/D: D:/WPC/Samples/Security/ParentalControls/UiExtRC/Debug/UiExtRC.dll,-106/e: c: \\ Windows \\Notepad.exe</span><span class="sxs-lookup"><span data-stu-id="10286-117">"D:\\WPC\\Samples\\Security\\ParentalControls\\UIExtensibility\\debug\\UIExtensibility" add /g:{FD59BB7F-54AB-11DB-9666-00E08161165F} /c:0 /n:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-101 /s:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-103 /i:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-104 /d:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-106 /e:c:\\windows\\Notepad.exe</span></span>

<span data-ttu-id="10286-118">где Уиекстрк — это простая Библиотека ресурсов с строковыми ресурсами для ИДЕНТИФИКАТОРов 101 и 103, а 24x24 Pixel 32 — bit с альфа-точечными рисунками для ресурсов 104 и 106.</span><span class="sxs-lookup"><span data-stu-id="10286-118">where UiExtRC is a simple resource DLL with string resources for ID's 101 and 103, and 24x24 pixel 32-bit with alpha bitmaps for resources 104 and 106.</span></span>

## <a name="webextensibility"></a><span data-ttu-id="10286-119">Расширение среды</span><span class="sxs-lookup"><span data-stu-id="10286-119">WebExtensibility</span></span>

<span data-ttu-id="10286-120">Консольное приложение, управляемое с помощью командной строки, демонстрирует использование API инструментария WMI и схемы WPC для перечисления, добавления и удаления записей HTTP-приложений или исключений URL-адресов, а также для установки и сброса переопределений фильтра веб-содержимого с помощью свойств Филтерид и FilterName.</span><span class="sxs-lookup"><span data-stu-id="10286-120">Command-line driven console application demonstrating how to use the WMI APIs and WPC schema to list, add, and delete HTTP application or URL exemption entries, and to set and reset a Web Content Filter override with the FilterID and FilterName properties.</span></span>

<span data-ttu-id="10286-121">Доступ к приложениям HTTP только для чтения и к спискам исключений URL-адресов не отображается, но код для чтения списков будет таким же, как в случае с чтением и записью, за исключением изменения параметра WMI.</span><span class="sxs-lookup"><span data-stu-id="10286-121">Access to the read-only HTTP application and URL exemption lists is not shown, but the code to read the lists would be the same as for the read/write case except for modification of the WMI parameter.</span></span>

 

 



