---
description: Пользовательское действие может вызывать функции, написанные на языке VBScript или JScript.
ms.assetid: d859713f-b8b8-4eb0-b678-52b5d880bd20
title: Скрипты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 114a11c12e94dd2f3285757bd01167f14b412ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673818"
---
# <a name="scripts"></a><span data-ttu-id="a4c6c-103">Скрипты</span><span class="sxs-lookup"><span data-stu-id="a4c6c-103">Scripts</span></span>

<span data-ttu-id="a4c6c-104">Пользовательское действие может вызывать функции, написанные на языке VBScript или JScript.</span><span class="sxs-lookup"><span data-stu-id="a4c6c-104">A custom action can call functions that are written in VBScript or JScript.</span></span> <span data-ttu-id="a4c6c-105">Установщик Windows не предоставляет обработчик скриптов.</span><span class="sxs-lookup"><span data-stu-id="a4c6c-105">Windows Installer does not provide the script engine.</span></span> <span data-ttu-id="a4c6c-106">Поэтому авторы, желающие использовать язык сценариев во время установки, должны обеспечить доступность соответствующего обработчика скриптов.</span><span class="sxs-lookup"><span data-stu-id="a4c6c-106">Authors wishing to make use of a scripting language during installation must therefore ensure that the appropriate scripting engine is available.</span></span>

<span data-ttu-id="a4c6c-107">Установщик не поддерживает JScript версии 1,0.</span><span class="sxs-lookup"><span data-stu-id="a4c6c-107">The installer does not support JScript version 1.0.</span></span>

<span data-ttu-id="a4c6c-108">64-разрядное пользовательское действие, основанное на скриптах, должно быть явно помечено как 64-разрядное настраиваемое действие путем добавления бита **msidbCustomActionType64BitScript** к числовому типу пользовательских действий в столбце Type таблицы [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a4c6c-108">A 64-bit custom action based on scripts must be explicitly marked as a 64-bit custom action by adding the **msidbCustomActionType64BitScript** bit to the custom actions numeric type in the Type column of the [CustomAction](customaction-table.md) table.</span></span> <span data-ttu-id="a4c6c-109">Дополнительные сведения см. в статье [64-разрядные пользовательские действия](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="a4c6c-109">For information see [64-Bit Custom Actions](64-bit-custom-actions.md).</span></span>

<span data-ttu-id="a4c6c-110">Следующие базовые типы пользовательских действий вызывают функции, написанные в скрипте.</span><span class="sxs-lookup"><span data-stu-id="a4c6c-110">The following basic custom action types call functions written in script.</span></span>



| <span data-ttu-id="a4c6c-111">Тип настраиваемого действия</span><span class="sxs-lookup"><span data-stu-id="a4c6c-111">Custom action type</span></span>                                 | <span data-ttu-id="a4c6c-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a4c6c-112">Description</span></span>                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4c6c-113">Тип настраиваемого действия 5</span><span class="sxs-lookup"><span data-stu-id="a4c6c-113">Custom Action Type 5</span></span>](custom-action-type-5.md)   | <span data-ttu-id="a4c6c-114">Файл JScript, хранящийся в потоке двоичных таблиц.</span><span class="sxs-lookup"><span data-stu-id="a4c6c-114">JScript file stored in a Binary table stream.</span></span>                                                  |
| [<span data-ttu-id="a4c6c-115">Тип настраиваемого действия 21</span><span class="sxs-lookup"><span data-stu-id="a4c6c-115">Custom Action Type 21</span></span>](custom-action-type-21.md) | <span data-ttu-id="a4c6c-116">Файл JScript, который устанавливается вместе с продуктом.</span><span class="sxs-lookup"><span data-stu-id="a4c6c-116">JScript file that is installed with a product.</span></span>                                                 |
| [<span data-ttu-id="a4c6c-117">Тип настраиваемого действия 53</span><span class="sxs-lookup"><span data-stu-id="a4c6c-117">Custom Action Type 53</span></span>](custom-action-type-53.md) | <span data-ttu-id="a4c6c-118">Текст JScript, заданный значением свойства.</span><span class="sxs-lookup"><span data-stu-id="a4c6c-118">JScript text specified by a property value.</span></span>                                                    |
| [<span data-ttu-id="a4c6c-119">Тип настраиваемого действия 37</span><span class="sxs-lookup"><span data-stu-id="a4c6c-119">Custom Action Type 37</span></span>](custom-action-type-37.md) | <span data-ttu-id="a4c6c-120">Текст JScript, хранящийся в целевом столбце таблицы [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a4c6c-120">JScript text stored in the Target column of the [CustomAction](customaction-table.md) table.</span></span>  |
| [<span data-ttu-id="a4c6c-121">Тип настраиваемого действия 6</span><span class="sxs-lookup"><span data-stu-id="a4c6c-121">Custom Action Type 6</span></span>](custom-action-type-6.md)   | <span data-ttu-id="a4c6c-122">Файл VBScript, хранящийся в потоке [двоичных](binary-table.md) таблиц.</span><span class="sxs-lookup"><span data-stu-id="a4c6c-122">VBScript file stored in a [Binary](binary-table.md) table stream.</span></span>                             |
| [<span data-ttu-id="a4c6c-123">Тип настраиваемого действия 22</span><span class="sxs-lookup"><span data-stu-id="a4c6c-123">Custom Action Type 22</span></span>](custom-action-type-22.md) | <span data-ttu-id="a4c6c-124">Файл VBScript, который устанавливается вместе с продуктом.</span><span class="sxs-lookup"><span data-stu-id="a4c6c-124">VBScript file that is installed with a product.</span></span>                                                |
| [<span data-ttu-id="a4c6c-125">Тип настраиваемого действия 54</span><span class="sxs-lookup"><span data-stu-id="a4c6c-125">Custom Action Type 54</span></span>](custom-action-type-54.md) | <span data-ttu-id="a4c6c-126">Текст VBScript, заданный значением свойства.</span><span class="sxs-lookup"><span data-stu-id="a4c6c-126">VBScript text specified by a property value.</span></span>                                                   |
| [<span data-ttu-id="a4c6c-127">Тип настраиваемого действия 38</span><span class="sxs-lookup"><span data-stu-id="a4c6c-127">Custom Action Type 38</span></span>](custom-action-type-38.md) | <span data-ttu-id="a4c6c-128">Текст VBScript, хранящийся в целевом столбце таблицы [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a4c6c-128">VBScript text stored in the Target column of the [CustomAction](customaction-table.md) table.</span></span> |



 

> [!Note]  
> <span data-ttu-id="a4c6c-129">Установщик выполняет пользовательские действия сценария напрямую и не использует сервер сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="a4c6c-129">The installer runs script custom actions directly and does not use the Windows Script Host.</span></span> <span data-ttu-id="a4c6c-130">Объект **Wscript** нельзя использовать внутри настраиваемого действия скрипта, так как этот объект предоставляется сервером сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="a4c6c-130">The **WScript** object cannot be used inside a script custom action because this object is provided by the Windows Script Host.</span></span> <span data-ttu-id="a4c6c-131">Объекты в объектной модели сервера сценариев Windows можно использовать только в пользовательских действиях, если на компьютере установлен сервер сценариев Windows, путем создания новых экземпляров объекта, вызова функции CreateObject и указания ProgId объекта (например, "WScript. Shell").</span><span class="sxs-lookup"><span data-stu-id="a4c6c-131">Objects in the Windows Script Host object model can only be used in custom actions if Windows Script Host is installed on the computer by creating new instances of the object, with a call to CreateObject, and providing the ProgId of the object (for example "WScript.Shell").</span></span> <span data-ttu-id="a4c6c-132">В зависимости от типа настраиваемого действия сценария доступ к некоторым объектам и методам объектной модели сервера сценариев Windows может быть запрещен по соображениям безопасности.</span><span class="sxs-lookup"><span data-stu-id="a4c6c-132">Depending on the type of script custom action, access to some objects and methods of the Windows Script Host object model may be denied for security reasons.</span></span>

 

<span data-ttu-id="a4c6c-133">Дополнительные сведения см. в разделе [сводный список всех типов настраиваемых действий](summary-list-of-all-custom-action-types.md) для сводки всех типов настраиваемых действий и их кодировки в таблице [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a4c6c-133">For more information, see [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a summary of all types of custom actions and how they are encoded into the [CustomAction](customaction-table.md) table.</span></span>

 

 



