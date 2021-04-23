---
description: Следующие интерфейсы используются приложением для управления пакетом печати документа.
ms.assetid: 576B4527-A753-4A73-899B-896DCB8B8945
title: Интерфейсы API для печати пакета документов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adc495be5c58598d00250568ff852cf4f897e0b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693517"
---
# <a name="print-document-package-api-interfaces"></a><span data-ttu-id="25898-103">Интерфейсы API для печати пакета документов</span><span class="sxs-lookup"><span data-stu-id="25898-103">Print Document Package API Interfaces</span></span>

<span data-ttu-id="25898-104">Следующие интерфейсы используются приложением для управления пакетом печати документа.</span><span class="sxs-lookup"><span data-stu-id="25898-104">The following interfaces are used by an app to manage the print document package.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="25898-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="25898-105">In this section</span></span>



| <span data-ttu-id="25898-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="25898-106">Topic</span></span>                                                                                       | <span data-ttu-id="25898-107">Описание</span><span class="sxs-lookup"><span data-stu-id="25898-107">Description</span></span>                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="25898-108">**ипринтдокументпаккажестатусевент**</span><span class="sxs-lookup"><span data-stu-id="25898-108">**IPrintDocumentPackageStatusEvent**</span></span>](/windows/desktop/api/Documenttarget/nn-documenttarget-iprintdocumentpackagestatusevent)<br/>     | <span data-ttu-id="25898-109">Представляет ход выполнения задания печати.</span><span class="sxs-lookup"><span data-stu-id="25898-109">Represents the progress of the print job.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="25898-110">**ипринтдокументпаккажетаржет**</span><span class="sxs-lookup"><span data-stu-id="25898-110">**IPrintDocumentPackageTarget**</span></span>](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)<br/>               | <span data-ttu-id="25898-111">Позволяет пользователям перечислять Поддерживаемые типы целевых объектов пакета и создавать их с заданным ИДЕНТИФИКАТОРом типа.</span><span class="sxs-lookup"><span data-stu-id="25898-111">Allows users to enumerate the supported package target types and to create one with a given type ID.</span></span> <span data-ttu-id="25898-112">**Ипринтдокументпаккажетаржет** также поддерживает отслеживание процесса печати пакета и его отмены.</span><span class="sxs-lookup"><span data-stu-id="25898-112">**IPrintDocumentPackageTarget** also supports the tracking of the package printing progress and cancelling.</span></span><br/> |
| [<span data-ttu-id="25898-113">**ипринтдокументпаккажетаржетфактори**</span><span class="sxs-lookup"><span data-stu-id="25898-113">**IPrintDocumentPackageTargetFactory**</span></span>](/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetargetfactory)<br/> | <span data-ttu-id="25898-114">Используется с [ипринтдокументпаккажетаржет](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) для запуска задания печати.</span><span class="sxs-lookup"><span data-stu-id="25898-114">Used with [IPrintDocumentPackageTarget](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) for starting a print job.</span></span><br/>                                                                                                               |



 

 

