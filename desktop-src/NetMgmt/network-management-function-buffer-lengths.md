---
title: Длина буфера функции управления сетью
description: В этом разделе обсуждаются требования к длине буфера функции при использовании с API управления сетью.
ms.assetid: 08599966-68a1-420b-bbc7-6daac833d08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5003f739d235a099adb9f4f403c15c67bd9169e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888468"
---
# <a name="network-management-function-buffer-lengths"></a><span data-ttu-id="a8ba6-103">Длина буфера функции управления сетью</span><span class="sxs-lookup"><span data-stu-id="a8ba6-103">Network Management Function Buffer Lengths</span></span>

<span data-ttu-id="a8ba6-104">В этом разделе обсуждаются требования к длине буфера функции при использовании с API управления сетью.</span><span class="sxs-lookup"><span data-stu-id="a8ba6-104">This topic discusses the requirements for function buffer lengths when used with the network management APIs.</span></span>

<span data-ttu-id="a8ba6-105">Приложения, которые задают размеры буфера при вызове функций перечисления управления сетью (и различных функций извлечения данных), должны указывать буферы, достаточные для хранения возвращаемой структуры данных (или структур), и строк, на которые они указывают.</span><span class="sxs-lookup"><span data-stu-id="a8ba6-105">Applications that specify buffer sizes when calling network management enumeration functions (and various data retrieval functions) must specify buffers large enough to hold the returned information structure (or structures) plus the strings to which their members point.</span></span> <span data-ttu-id="a8ba6-106">Если не указать достаточно большой буфер для получения всех доступных записей, функция возвращает ошибку \_ больше \_ данных.</span><span class="sxs-lookup"><span data-stu-id="a8ba6-106">If you do not specify a large enough buffer to receive all the available entries, the function returns ERROR\_MORE\_DATA.</span></span> <span data-ttu-id="a8ba6-107">Вызовы перечисления не возвращают частичные записи.</span><span class="sxs-lookup"><span data-stu-id="a8ba6-107">Enumeration calls do not return partial entries.</span></span>

<span data-ttu-id="a8ba6-108">Некоторые функции управления сетью принимают рекомендации с максимальным значением длины данных, *префмакслен*.</span><span class="sxs-lookup"><span data-stu-id="a8ba6-108">Some network management functions take an advisory maximum data-length parameter, *prefmaxlen*.</span></span> <span data-ttu-id="a8ba6-109">Этот параметр позволяет приложению предложить количество байтов, возвращаемых сервером из вызова функции.</span><span class="sxs-lookup"><span data-stu-id="a8ba6-109">This parameter allows an application to suggest the number of bytes the server should return from a function call.</span></span>

<span data-ttu-id="a8ba6-110">Если \_ в параметре префмакслен указать значение максимальной предпочтительной \_ длины, функции управления сетью распределяют объем памяти, необходимый для данных. </span><span class="sxs-lookup"><span data-stu-id="a8ba6-110">If you specify the value MAX\_PREFERRED\_LENGTH in the *prefmaxlen* parameter, the network management functions allocate the amount of memory required for the data.</span></span>

<span data-ttu-id="a8ba6-111">Дополнительные сведения см. в разделе [буферы функций управления сетью](network-management-function-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="a8ba6-111">For more information, see [Network Management Function Buffers](network-management-function-buffers.md).</span></span>

 

 




