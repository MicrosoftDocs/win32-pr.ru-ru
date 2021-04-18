---
title: Поставщик средства оценки системы Windows
description: Средство Windows System оценке (WinSAT) предоставляет ряд классов, оценивающих характеристики и возможности производительности компьютера.
ms.assetid: f0ce8b55-25b4-40fa-b17f-32a021b50395
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6ccd6430ec13132181bd00f190b00ef4d3a1506
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700537"
---
# <a name="windows-system-assessment-tool-provider"></a><span data-ttu-id="65b95-103">Поставщик средства оценки системы Windows</span><span class="sxs-lookup"><span data-stu-id="65b95-103">Windows System Assessment Tool Provider</span></span>

<span data-ttu-id="65b95-104">\[Служба WinSAT может быть изменена или недоступна для выпусков после Windows 8.1.\]</span><span class="sxs-lookup"><span data-stu-id="65b95-104">\[WinSAT may be altered or unavailable for releases after Windows 8.1.\]</span></span>

## <a name="purpose"></a><span data-ttu-id="65b95-105">Назначение</span><span class="sxs-lookup"><span data-stu-id="65b95-105">Purpose</span></span>

<span data-ttu-id="65b95-106">Средство Windows System оценке (WinSAT) предоставляет ряд классов, оценивающих характеристики и возможности производительности компьютера.</span><span class="sxs-lookup"><span data-stu-id="65b95-106">The Windows System Assessment Tool (WinSAT) exposes a number of classes that assesses the performance characteristics and capabilities of a computer.</span></span> <span data-ttu-id="65b95-107">Разработчики могут использовать этот API для разработки программного обеспечения, которое может получать доступ к сведениям о производительности и возможностях компьютера для определения оптимальных параметров приложения на основе возможностей производительности этого компьютера.</span><span class="sxs-lookup"><span data-stu-id="65b95-107">Developers can use this API to develop software that can access the performance and capability information of a computer to determine the optimal application settings based on that computer's performance capabilities.</span></span>

<span data-ttu-id="65b95-108">Пользователи могут использовать результаты формальной оценки, чтобы определить, какие сценарии и приложения будут хорошо работать на компьютере.</span><span class="sxs-lookup"><span data-stu-id="65b95-108">Users can use the results of a formal assessment to determine which scenarios and applications will perform well on a computer.</span></span> <span data-ttu-id="65b95-109">Например, если пакет программного обеспечения содержит оценку его упаковки, пользователь может использовать рейтинг, чтобы определить, будет ли программное обеспечение правильно работать на компьютере.</span><span class="sxs-lookup"><span data-stu-id="65b95-109">For example, if a software package contains a rating on its packaging, a user can use the rating to determine whether the software will run well on the computer.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="65b95-110">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="65b95-110">Developer audience</span></span>

<span data-ttu-id="65b95-111">Служба WinSAT разработана для разработчиков на C, C++ и Visual Basic, а также для тех, кто пишет сценарии.</span><span class="sxs-lookup"><span data-stu-id="65b95-111">WinSAT is designed for C, C++, and Visual Basic developers and those who write scripts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="65b95-112">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="65b95-112">Run-time requirements</span></span>

<span data-ttu-id="65b95-113">Служба WinSAT доступна на клиентских компьютерах, начиная с операционной системы Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="65b95-113">WinSAT is available on client computers starting with the Windows Vista operating system.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="65b95-114">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="65b95-114">In this section</span></span>



| <span data-ttu-id="65b95-115">Раздел</span><span class="sxs-lookup"><span data-stu-id="65b95-115">Topic</span></span>                                               | <span data-ttu-id="65b95-116">Описание</span><span class="sxs-lookup"><span data-stu-id="65b95-116">Description</span></span>                                                                                                   |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65b95-117">Использование WinSAT</span><span class="sxs-lookup"><span data-stu-id="65b95-117">Using WinSAT</span></span>](using-winsat.md)<br/>         | <span data-ttu-id="65b95-118">Процедурное пошаговое описание для оценки инициации, получения оценок и получения сведений о оценке.</span><span class="sxs-lookup"><span data-stu-id="65b95-118">Procedural guide for initiating assessments, retrieving scores, and retrieving assessment details.</span></span><br/> |
| [<span data-ttu-id="65b95-119">Справочник по службе WinSAT</span><span class="sxs-lookup"><span data-stu-id="65b95-119">WinSAT Reference</span></span>](winsat-reference.md)<br/> | <span data-ttu-id="65b95-120">Справочные сведения об API-интерфейсе WinSAT, примерах и схеме.</span><span class="sxs-lookup"><span data-stu-id="65b95-120">Reference information for the WinSAT API, samples, and schema.</span></span> <br/>                                    |



 

 

 





