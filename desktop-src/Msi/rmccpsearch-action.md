---
description: Действие Рмккпсеарч использует подписи файлов для проверки того, что соответствующие продукты установлены в системе до выполнения установки обновления.
ms.assetid: d37b2434-86eb-4c6e-b817-77c75dcebbf5
title: Действие Рмккпсеарч
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c273ccb03bb77e0346edf73177d938d6002878a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673496"
---
# <a name="rmccpsearch-action"></a><span data-ttu-id="d1923-103">Действие Рмккпсеарч</span><span class="sxs-lookup"><span data-stu-id="d1923-103">RMCCPSearch Action</span></span>

<span data-ttu-id="d1923-104">Действие Рмккпсеарч использует подписи файлов для проверки того, что соответствующие продукты установлены в системе до выполнения установки обновления.</span><span class="sxs-lookup"><span data-stu-id="d1923-104">The RMCCPSearch action uses file signatures to validate that qualifying products are installed on a system before an upgrade installation is performed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d1923-105">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="d1923-105">Sequence Restrictions</span></span>

<span data-ttu-id="d1923-106">Действие Рмккпсеарч должно быть создано в [таблице инсталлуисекуенце](installuisequence-table.md) и [таблице инсталлексекутесекуенце](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="d1923-106">RMCCPSearch action should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="d1923-107">Установщик предотвращает выполнение Рмккпсеарч в последовательности Инсталлексекутесекуенце, если действие уже выполнялось в последовательности Инсталлуисекуенце.</span><span class="sxs-lookup"><span data-stu-id="d1923-107">The installer prevents RMCCPSearch from running in the InstallExecuteSequence sequence if the action has already run in InstallUISequence sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="d1923-108">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="d1923-108">ActionData Messages</span></span>

<span data-ttu-id="d1923-109">Нет сообщений Актиондата.</span><span class="sxs-lookup"><span data-stu-id="d1923-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1923-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d1923-110">Remarks</span></span>

<span data-ttu-id="d1923-111">Для действия Рмккпсеарч необходимо, чтобы свойство [**\_ диска CCP**](ccp-drive.md) было установлено в корневой путь на съемном [*томе*](v-gly.md) , на котором установлена установка для любого из соответствующих продуктов.</span><span class="sxs-lookup"><span data-stu-id="d1923-111">The RMCCPSearch action requires the [**CCP\_DRIVE**](ccp-drive.md) property to be set to the root path on the removable [*volume*](v-gly.md) that has the installation for any of the qualifying products.</span></span>

<span data-ttu-id="d1923-112">Каждая подпись файла в таблице Ккпсеарч ищется по пути, указанному свойством [**CCP \_ Drive**](ccp-drive.md) , с помощью таблицы [дрлокатор](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="d1923-112">Each file signature in the CCPSearch table is searched for under the path referred to by the [**CCP\_DRIVE**](ccp-drive.md) property using the [DrLocator](drlocator-table.md) table.</span></span> <span data-ttu-id="d1923-113">Отсутствие подписи в таблице [сигнатур](signature-table.md) указывает на каталог.</span><span class="sxs-lookup"><span data-stu-id="d1923-113">The absence of the signature from the [Signature](signature-table.md) table denotes a directory.</span></span> <span data-ttu-id="d1923-114">Если какая-либо сигнатура определена как существующая, действие Рмккпсеарч завершается.</span><span class="sxs-lookup"><span data-stu-id="d1923-114">If any signature is determined to exist, the RMCCPSearch action terminates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1923-115">См. также</span><span class="sxs-lookup"><span data-stu-id="d1923-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1923-116">Таблица Ккпсеарч</span><span class="sxs-lookup"><span data-stu-id="d1923-116">CCPSearch table</span></span>](ccpsearch-table.md)
</dt> </dl>

 

 



