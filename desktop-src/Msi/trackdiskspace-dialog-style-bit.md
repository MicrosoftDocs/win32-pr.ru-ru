---
description: Если этот бит задан, диалоговое окно периодически вызывает установщик.
ms.assetid: 7798cb50-72e4-4530-bf06-1927dd963a01
title: Бит стиля диалогового окна Траккдискспаце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eab0cf234071ace41432e20a598b38fb1fc431e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143441"
---
# <a name="trackdiskspace-dialog-style-bit"></a><span data-ttu-id="14bbf-103">Бит стиля диалогового окна Траккдискспаце</span><span class="sxs-lookup"><span data-stu-id="14bbf-103">TrackDiskSpace Dialog Style Bit</span></span>

<span data-ttu-id="14bbf-104">Если этот бит задан, диалоговое окно периодически вызывает установщик.</span><span class="sxs-lookup"><span data-stu-id="14bbf-104">If this bit is set, the dialog box periodically calls the installer.</span></span> <span data-ttu-id="14bbf-105">Если свойство изменяется, оно уведомляет элементы управления в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="14bbf-105">If the property changes, it notifies the controls on the dialog.</span></span> <span data-ttu-id="14bbf-106">Этот стиль можно использовать, если в диалоговом окне есть элемент управления, указывающий место на диске.</span><span class="sxs-lookup"><span data-stu-id="14bbf-106">This style can be used if there is a control on the dialog indicating disk space.</span></span> <span data-ttu-id="14bbf-107">Если пользователь переключается на другое приложение, добавляет или удаляет файлы или иным образом изменяет доступное место на диске, можно быстро реализовать изменение с помощью этого стиля.</span><span class="sxs-lookup"><span data-stu-id="14bbf-107">If the user switches to another application, adds or removes files, or otherwise modifies available disk space, you can quickly implement the change using this style.</span></span>

<span data-ttu-id="14bbf-108">Любое диалоговое окно, использующее свойство [**аутофдискспаце**](outofdiskspace.md) для определения, должен ли открыться диалоговое окно, должно установить бит стиля диалогового окна траккдискспаце для диалогового окна, чтобы динамически обновлять пространство на целевых томах.</span><span class="sxs-lookup"><span data-stu-id="14bbf-108">Any dialog box relying on the [**OutOfDiskSpace**](outofdiskspace.md) property to determine whether to bring up a dialog must set the TrackDiskSpace Dialog Style Bit for the dialog to dynamically update space on the target volumes.</span></span>

## <a name="value"></a><span data-ttu-id="14bbf-109">Значение</span><span class="sxs-lookup"><span data-stu-id="14bbf-109">Value</span></span>



| <span data-ttu-id="14bbf-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="14bbf-110">Decimal</span></span> | <span data-ttu-id="14bbf-111">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="14bbf-111">Hexadecimal</span></span> | <span data-ttu-id="14bbf-112">Константа</span><span class="sxs-lookup"><span data-stu-id="14bbf-112">Constant</span></span>                                |
|---------|-------------|-----------------------------------------|
| <span data-ttu-id="14bbf-113">32</span><span class="sxs-lookup"><span data-stu-id="14bbf-113">32</span></span>      | <span data-ttu-id="14bbf-114">0x00000020</span><span class="sxs-lookup"><span data-stu-id="14bbf-114">0x00000020</span></span>  | <span data-ttu-id="14bbf-115">**мсидбдиалогаттрибутестраккдискспаце**</span><span class="sxs-lookup"><span data-stu-id="14bbf-115">**msidbDialogAttributesTrackDiskSpace**</span></span> |



 

 

 



