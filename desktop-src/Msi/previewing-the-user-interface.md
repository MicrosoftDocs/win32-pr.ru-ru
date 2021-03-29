---
description: Установщик сохраняет все сведения о пользовательском интерфейсе в таблицах базы данных установки.
ms.assetid: 56d8ecb4-6c95-46c6-98dc-3118d2061101
title: Предварительный просмотр пользовательского интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c58f30dcd797064ef9b01217927fda96a758f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264836"
---
# <a name="previewing-the-user-interface"></a><span data-ttu-id="98ecd-103">Предварительный просмотр пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="98ecd-103">Previewing the User Interface</span></span>

<span data-ttu-id="98ecd-104">Установщик сохраняет все сведения о [пользовательском интерфейсе](user-interface.md) в таблицах базы данных установки.</span><span class="sxs-lookup"><span data-stu-id="98ecd-104">The installer stores all information about the [user interface](user-interface.md) in the tables of the installation database.</span></span> <span data-ttu-id="98ecd-105">Для упрощения разработки пользовательского интерфейса установщик также предоставляет режим предварительного просмотра для просмотра этих сведений.</span><span class="sxs-lookup"><span data-stu-id="98ecd-105">To facilitate the design of the UI the installer also provides a preview mode for viewing this information.</span></span> <span data-ttu-id="98ecd-106">В следующей процедуре описывается включение режима предварительного просмотра пользовательского интерфейса и отображение текущего внешнего вида диалоговых окон и объявлений.</span><span class="sxs-lookup"><span data-stu-id="98ecd-106">The following procedure describes how to enable the UI preview mode and display the current appearance of dialog boxes and billboards.</span></span>

<span data-ttu-id="98ecd-107">**Просмотр пользовательского интерфейса в режиме предварительного просмотра**</span><span class="sxs-lookup"><span data-stu-id="98ecd-107">**To view the user interface in the preview mode**</span></span>

1.  <span data-ttu-id="98ecd-108">Включите режим предварительного просмотра, вызвав функцию [**мсиенаблеуипревиев**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview) .</span><span class="sxs-lookup"><span data-stu-id="98ecd-108">Enable the preview mode by calling the [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview) function.</span></span>
2.  <span data-ttu-id="98ecd-109">Отображение определенных диалоговых окон путем вызова функции [**мсипревиевдиалог**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga) .</span><span class="sxs-lookup"><span data-stu-id="98ecd-109">Display the particular dialog boxes by calling the [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga) function.</span></span>
3.  <span data-ttu-id="98ecd-110">Отображение определенных объявлений путем вызова функции [**мсипревиевбиллбоард**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) .</span><span class="sxs-lookup"><span data-stu-id="98ecd-110">Display particular billboards by calling the [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) function.</span></span>

 

 



