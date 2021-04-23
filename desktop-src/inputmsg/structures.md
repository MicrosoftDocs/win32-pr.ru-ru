---
title: Структуры (входные сообщения указателя и уведомления)
description: В подразделах этого раздела приведены справочные спецификации для входных сообщений указателя и структур уведомлений.
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114801138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: bc796c3924df9a1a349ea2180123f88f56d6a96c
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/26/2021
ms.locfileid: "105721069"
---
# <a name="pointer-input-messages-and-notifications-structures"></a><span data-ttu-id="4fc9c-103">Входные сообщения указателя и структуры уведомлений</span><span class="sxs-lookup"><span data-stu-id="4fc9c-103">Pointer Input Messages and Notifications structures</span></span>

<span data-ttu-id="4fc9c-104">В подразделах этого раздела приведены справочные спецификации для [входных сообщений указателя и структур уведомлений](messages-and-notifications-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="4fc9c-104">The topics in this section provide the reference specifications for [Pointer Input Messages and Notifications](messages-and-notifications-portal.md) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4fc9c-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="4fc9c-105">In this section</span></span>



| <span data-ttu-id="4fc9c-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="4fc9c-106">Topic</span></span>                                                                            | <span data-ttu-id="4fc9c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="4fc9c-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4fc9c-108">**INPUT_TRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="4fc9c-108">**INPUT_TRANSFORM**</span></span>](/previous-versions/windows/desktop/api)<br/>                           | <span data-ttu-id="4fc9c-109">Определяет матрицу, которая представляет преобразование в потребителе сообщения.</span><span class="sxs-lookup"><span data-stu-id="4fc9c-109">Defines the matrix that represents a transform on a message consumer.</span></span> <span data-ttu-id="4fc9c-110">Эта матрица может использоваться для преобразования входных данных указателя от клиентских координат к координатам экрана, а обратная возможность — для преобразования входных данных указателя из координат экрана в клиентские координаты.</span><span class="sxs-lookup"><span data-stu-id="4fc9c-110">This matrix can be used to transform pointer input data from client coordinates to screen coordinates, while the inverse can be used to transform pointer input data from screen coordinates to client coordinates.</span></span> <br/>                                                                 |
| [<span data-ttu-id="4fc9c-111">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="4fc9c-111">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)<br/>                          | <span data-ttu-id="4fc9c-112">Содержит основные сведения о указателе, общие для всех типов указателей.</span><span class="sxs-lookup"><span data-stu-id="4fc9c-112">Contains basic pointer information common to all pointer types.</span></span> <span data-ttu-id="4fc9c-113">Приложения могут получать эти сведения с помощью функций [**жетпоинтеринфо**](/previous-versions/windows/desktop/api), [**жетпоинтерфрамеинфо**](/previous-versions/windows/desktop/api), [**жетпоинтеринфохистори**](/previous-versions/windows/desktop/api) и [**жетпоинтерфрамеинфохистори**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="4fc9c-113">Applications can retrieve this information using the [**GetPointerInfo**](/previous-versions/windows/desktop/api), [**GetPointerFrameInfo**](/previous-versions/windows/desktop/api), [**GetPointerInfoHistory**](/previous-versions/windows/desktop/api) and [**GetPointerFrameInfoHistory**](/previous-versions/windows/desktop/api) functions.</span></span> <br/> |
| [<span data-ttu-id="4fc9c-114">**POINTER_PEN_INFO**</span><span class="sxs-lookup"><span data-stu-id="4fc9c-114">**POINTER_PEN_INFO**</span></span>](/previous-versions/windows/desktop/api)<br/>                 | <span data-ttu-id="4fc9c-115">Определяет основные сведения о пере, общие для всех типов указателей.</span><span class="sxs-lookup"><span data-stu-id="4fc9c-115">Defines basic pen information common to all pointer types.</span></span> <br/>                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="4fc9c-116">**POINTER_TOUCH_INFO**</span><span class="sxs-lookup"><span data-stu-id="4fc9c-116">**POINTER_TOUCH_INFO**</span></span>](/previous-versions/windows/desktop/api)<br/>             | <span data-ttu-id="4fc9c-117">Определяет основные сведения о сенсорном вводе, общие для всех типов указателей.</span><span class="sxs-lookup"><span data-stu-id="4fc9c-117">Defines basic touch information common to all pointer types.</span></span><br/>                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="4fc9c-118">**таучпредиктионпараметерс**</span><span class="sxs-lookup"><span data-stu-id="4fc9c-118">**TOUCHPREDICTIONPARAMETERS**</span></span>](/previous-versions/windows/desktop/api)<br/> | <span data-ttu-id="4fc9c-119">Содержит сведения о входных данных оборудования, которые могут использоваться для прогнозирования мишеней касаний и помогают компенсировать задержку оборудования при обработке сенсорного ввода и данных, содержащих расстояние и скорость.</span><span class="sxs-lookup"><span data-stu-id="4fc9c-119">Contains hardware input details that can be used to predict touch targets and help compensate for hardware latency when processing touch and gesture input that contains distance and velocity data.</span></span><br/>                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="4fc9c-120">См. также</span><span class="sxs-lookup"><span data-stu-id="4fc9c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fc9c-121">Ссылка на входящее сообщение указателя</span><span class="sxs-lookup"><span data-stu-id="4fc9c-121">Pointer Input Message Reference</span></span>](wmpointer-reference.md)
</dt> </dl>

 

 





