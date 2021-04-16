---
description: Действие Ккпсеарч использует подписи файлов для проверки того, что соответствующие продукты установлены в системе до выполнения установки обновления.
ms.assetid: 0aa7bf8b-de76-464d-8e7b-3aa4f609fe19
title: Действие Ккпсеарч
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8b1f01462ac0ba9dcf8838b9a043d95aef8cefe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650709"
---
# <a name="ccpsearch-action"></a><span data-ttu-id="589d3-103">Действие Ккпсеарч</span><span class="sxs-lookup"><span data-stu-id="589d3-103">CCPSearch Action</span></span>

<span data-ttu-id="589d3-104">Действие Ккпсеарч использует подписи файлов для проверки того, что соответствующие продукты установлены в системе до выполнения установки обновления.</span><span class="sxs-lookup"><span data-stu-id="589d3-104">The CCPSearch action uses file signatures to validate that qualifying products are installed on a system before an upgrade installation is performed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="589d3-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="589d3-105">Sequence Restrictions</span></span>

<span data-ttu-id="589d3-106">Действие Ккпсеарч должно быть создано в [таблице инсталлуисекуенце](installuisequence-table.md) и [таблице инсталлексекутесекуенце](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="589d3-106">CCPSearch action should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="589d3-107">Установщик предотвращает выполнение действия Ккпсеарч в последовательности Инсталлексекутесекуенце, если действие уже выполнялось в последовательности Инсталлуисекуенце.</span><span class="sxs-lookup"><span data-stu-id="589d3-107">The installer prevents the CCPSearch action from running in the InstallExecuteSequence sequence if the action has already run in InstallUISequence sequence.</span></span> <span data-ttu-id="589d3-108">Действие Ккпсеарч должно следовать перед действием [рмккпсеарч](rmccpsearch-action.md) .</span><span class="sxs-lookup"><span data-stu-id="589d3-108">The CCPSearch action must come before the [RMCCPSearch](rmccpsearch-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="589d3-109">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="589d3-109">ActionData Messages</span></span>

<span data-ttu-id="589d3-110">Нет сообщений Актиондата.</span><span class="sxs-lookup"><span data-stu-id="589d3-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="589d3-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="589d3-111">Remarks</span></span>

<span data-ttu-id="589d3-112">Действие Ккпсеарч ищет подписи файлов, перечисленные в таблице Ккпсеарч в системе, используя следующие таблицы в порядке: Signature, Комплокатор, Реглокатор, Инилокатор и Дрлокатор.</span><span class="sxs-lookup"><span data-stu-id="589d3-112">The CCPSearch action searches for file signatures listed in the CCPSearch table on the system using the following tables in order: Signature, CompLocator, RegLocator, IniLocator, and DrLocator.</span></span>

<span data-ttu-id="589d3-113">Если определена какая-либо сигнатура, свойство **CCP \_ Success** устанавливается в значение 1, а действие ккпсеарч завершается.</span><span class="sxs-lookup"><span data-stu-id="589d3-113">If any signature is determined to exist, the **CCP\_Success** property is set to 1 and the CCPSearch action terminates.</span></span>

<span data-ttu-id="589d3-114">Отсутствие подписи в таблице сигнатур указывает на каталог.</span><span class="sxs-lookup"><span data-stu-id="589d3-114">The absence of the signature from the Signature table denotes a directory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="589d3-115">См. также</span><span class="sxs-lookup"><span data-stu-id="589d3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="589d3-116">ккпсеарч</span><span class="sxs-lookup"><span data-stu-id="589d3-116">CCPSearch</span></span>](ccpsearch-table.md)
</dt> <dt>

[<span data-ttu-id="589d3-117">Образец</span><span class="sxs-lookup"><span data-stu-id="589d3-117">Signature</span></span>](signature-table.md)
</dt> <dt>

[<span data-ttu-id="589d3-118">комплокатор</span><span class="sxs-lookup"><span data-stu-id="589d3-118">CompLocator</span></span>](complocator-table.md)
</dt> <dt>

[<span data-ttu-id="589d3-119">реглокатор</span><span class="sxs-lookup"><span data-stu-id="589d3-119">RegLocator</span></span>](reglocator-table.md)
</dt> <dt>

[<span data-ttu-id="589d3-120">инилокатор</span><span class="sxs-lookup"><span data-stu-id="589d3-120">IniLocator</span></span>](inilocator-table.md)
</dt> <dt>

[<span data-ttu-id="589d3-121">дрлокатор</span><span class="sxs-lookup"><span data-stu-id="589d3-121">DrLocator</span></span>](drlocator-table.md)
</dt> </dl>

 

 



