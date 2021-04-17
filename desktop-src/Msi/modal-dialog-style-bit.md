---
description: Если этот бит задан, диалоговое окно является модальным, другие диалоговые окна того же приложения не могут быть поверх него, а диалоговое окно сохраняет элемент управления во время его работы.
ms.assetid: 14871dc7-c928-4381-a043-6beb06d25214
title: Бит модального стиля диалогового окна
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd0004cc7b31557f9a606050a1f8569fa2a493d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546359"
---
# <a name="modal-dialog-style-bit"></a><span data-ttu-id="18aae-103">Бит модального стиля диалогового окна</span><span class="sxs-lookup"><span data-stu-id="18aae-103">Modal Dialog Style Bit</span></span>

<span data-ttu-id="18aae-104">Если этот бит задан, диалоговое окно является модальным, другие диалоговые окна того же приложения не могут быть поверх него, а диалоговое окно сохраняет элемент управления во время его работы.</span><span class="sxs-lookup"><span data-stu-id="18aae-104">If this bit is set, the dialog box is modal, other dialogs of the same application cannot be put on top of it, and the dialog keeps the control while it is running.</span></span> <span data-ttu-id="18aae-105">Если этот бит не задан, диалоговое окно немодальное, и другие диалоговые окна этого же приложения могут быть перемещены поверх него.</span><span class="sxs-lookup"><span data-stu-id="18aae-105">If this bit is not set, the dialog is modeless, other dialogs of the same application may be moved on top of it.</span></span> <span data-ttu-id="18aae-106">После создания и отображения немодального диалогового окна Пользовательский интерфейс возвращает управление установщику.</span><span class="sxs-lookup"><span data-stu-id="18aae-106">After a modeless dialog is created and displayed, the user interface returns control to the installer.</span></span> <span data-ttu-id="18aae-107">Затем установщик периодически вызывает пользовательский интерфейс, чтобы обновить диалоговое окно и дать ему возможность обработать сообщения.</span><span class="sxs-lookup"><span data-stu-id="18aae-107">The installer then calls the user interface periodically to update the dialog and to give it a chance to process the messages.</span></span> <span data-ttu-id="18aae-108">Как только это будет сделано, элемент управления возвращается в установщик.</span><span class="sxs-lookup"><span data-stu-id="18aae-108">As soon as this is done, the control is returned to the installer.</span></span>

> [!Note]  
> <span data-ttu-id="18aae-109">В последовательности мастера не должно быть безрежимных диалоговых окон, так как при этом будет возвращено управление установщиком, преждевременно Завершая последовательность мастера.</span><span class="sxs-lookup"><span data-stu-id="18aae-109">There should be no modeless dialogs in a wizard sequence, since this would return control to the installer, ending the wizard sequence prematurely.</span></span>

 

## <a name="value"></a><span data-ttu-id="18aae-110">Значение</span><span class="sxs-lookup"><span data-stu-id="18aae-110">Value</span></span>



| <span data-ttu-id="18aae-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="18aae-111">Decimal</span></span> | <span data-ttu-id="18aae-112">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="18aae-112">Hexadecimal</span></span> | <span data-ttu-id="18aae-113">Константа</span><span class="sxs-lookup"><span data-stu-id="18aae-113">Constant</span></span>                          |
|---------|-------------|-----------------------------------|
| <span data-ttu-id="18aae-114">2</span><span class="sxs-lookup"><span data-stu-id="18aae-114">2</span></span>       | <span data-ttu-id="18aae-115">0x00000002</span><span class="sxs-lookup"><span data-stu-id="18aae-115">0x00000002</span></span>  | <span data-ttu-id="18aae-116">**мсидбдиалогаттрибутессисмодал**</span><span class="sxs-lookup"><span data-stu-id="18aae-116">**msidbDialogAttributesSysModal**</span></span> |



 

 

 



