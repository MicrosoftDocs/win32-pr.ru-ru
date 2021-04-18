---
description: Действие Ремоверегистривалуес может удалять только значения из системного реестра, созданные в таблице реестра или таблице Ремоверегистри.
ms.assetid: aa05eb75-15f2-4e2a-a8e2-a770ad078b41
title: Действие Ремоверегистривалуес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e6e7473be344faa08ed456e72e3b9c80c4aa8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663576"
---
# <a name="removeregistryvalues-action"></a><span data-ttu-id="49378-103">Действие Ремоверегистривалуес</span><span class="sxs-lookup"><span data-stu-id="49378-103">RemoveRegistryValues Action</span></span>

<span data-ttu-id="49378-104">Действие Ремоверегистривалуес может удалять только значения из системного реестра, созданные в [таблице реестра](registry-table.md) или [таблице ремоверегистри](removeregistry-table.md).</span><span class="sxs-lookup"><span data-stu-id="49378-104">The RemoveRegistryValues action can only remove values from the system registry that have been authored into the [Registry table](registry-table.md) or the [RemoveRegistry table](removeregistry-table.md).</span></span> <span data-ttu-id="49378-105">Это действие удаляет значение реестра, созданное в таблице реестра, если связанный компонент был установлен локально или запущен из источника и теперь настроен для удаления.</span><span class="sxs-lookup"><span data-stu-id="49378-105">This action removes a registry value that has been authored into the Registry table if the associated component was installed locally or as run from source and is now set to be uninstalled.</span></span> <span data-ttu-id="49378-106">Это действие удаляет значение реестра, созданное в таблице Ремоверегистри, если соответствующий компонент настроен на локальную установку или запуск из источника.</span><span class="sxs-lookup"><span data-stu-id="49378-106">This action removes a registry value that has been authored into the RemoveRegistry table if the associated component is set to be installed locally or as run from source.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="49378-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="49378-107">Sequence Restrictions</span></span>

<span data-ttu-id="49378-108">Перед вызовом Ремоверегистривалуес необходимо вызвать действие [инсталлвалидате](installvalidate-action.md) .</span><span class="sxs-lookup"><span data-stu-id="49378-108">The [InstallValidate](installvalidate-action.md) action must be called before calling RemoveRegistryValues.</span></span> <span data-ttu-id="49378-109">Если используется действие [вритерегистривалуес](writeregistryvalues-action.md) , оно должно следовать после ремоверегистривалуес.</span><span class="sxs-lookup"><span data-stu-id="49378-109">If a [WriteRegistryValues](writeregistryvalues-action.md) action is used, it must come after RemoveRegistryValues.</span></span> <span data-ttu-id="49378-110">Ремоверегистривалуес должен идти перед [унрегистермимеинфо](unregistermimeinfo-action.md) или [унрегистерпрогидинфо](unregisterprogidinfo-action.md).</span><span class="sxs-lookup"><span data-stu-id="49378-110">RemoveRegistryValues must come before [UnregisterMIMEInfo](unregistermimeinfo-action.md) or [UnregisterProgIDInfo](unregisterprogidinfo-action.md).</span></span>

<span data-ttu-id="49378-111">Пользовательское действие можно использовать для добавления строк в [таблицу реестра](registry-table.md) во время установки, удаления или восстановления транзакции.</span><span class="sxs-lookup"><span data-stu-id="49378-111">A custom action can be used to add rows to the [Registry table](registry-table.md) during an installation, uninstallation, or repair transaction.</span></span> <span data-ttu-id="49378-112">Эти строки не сохраняются в таблице реестра, и эти данные доступны только во время текущей транзакции.</span><span class="sxs-lookup"><span data-stu-id="49378-112">These rows do not persist in the Registry table and the information is only available during the current transaction.</span></span> <span data-ttu-id="49378-113">Поэтому пользовательское действие должно выполняться при каждой установке, удалении или исправлении транзакций, для которых требуется информация в этих дополнительных строках.</span><span class="sxs-lookup"><span data-stu-id="49378-113">The custom action must therefore be run in every installation, uninstallation, or repair transaction that requires the information in these additional rows.</span></span> <span data-ttu-id="49378-114">Пользовательское действие должно предшествовать действиям Ремоверегистривалуес и [вритерегистривалуес](writeregistryvalues-action.md) в последовательности действий.</span><span class="sxs-lookup"><span data-stu-id="49378-114">The custom action must come before the RemoveRegistryValues and [WriteRegistryValues](writeregistryvalues-action.md) actions in the action sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="49378-115">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="49378-115">ActionData Messages</span></span>



| <span data-ttu-id="49378-116">Поле</span><span class="sxs-lookup"><span data-stu-id="49378-116">Field</span></span> | <span data-ttu-id="49378-117">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="49378-117">Description of action data</span></span>                          |
|-------|-----------------------------------------------------|
| <span data-ttu-id="49378-118">\[1\]</span><span class="sxs-lookup"><span data-stu-id="49378-118">\[1\]</span></span> | <span data-ttu-id="49378-119">Путь реестра к ключу удаленного значения реестра.</span><span class="sxs-lookup"><span data-stu-id="49378-119">Registry path to key of removed registry value.</span></span>     |
| <span data-ttu-id="49378-120">\[2\]</span><span class="sxs-lookup"><span data-stu-id="49378-120">\[2\]</span></span> | <span data-ttu-id="49378-121">Форматированная строка имени удаленного значения реестра.</span><span class="sxs-lookup"><span data-stu-id="49378-121">Formatted string of name of removed registry value.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="49378-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49378-122">Remarks</span></span>

<span data-ttu-id="49378-123">Чтобы удалить значение реестра, запишите значение в столбце значение таблицы реестра.</span><span class="sxs-lookup"><span data-stu-id="49378-123">To remove a registry value, record the value in the Value column of the Registry table.</span></span> <span data-ttu-id="49378-124">Если действие Вритерегистривалуес прикрепляет \_ несколько строк REG \_ SZ к значению в [таблице реестра](registry-table.md), то действие ремоверегистривалуес удаляет только строки из значения реестра.</span><span class="sxs-lookup"><span data-stu-id="49378-124">If the WriteRegistryValues action has attached REG\_MULTI\_SZ strings to the value in the [Registry table](registry-table.md), then the RemoveRegistryValues action removes only those strings from the registry value.</span></span>

 

 



