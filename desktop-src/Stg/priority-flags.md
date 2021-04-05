---
title: Флаги приоритета
description: Флаг приоритета открывает объект хранилища в режиме приоритета.
ms.assetid: 85f2df6f-9219-4752-8c17-f219c37a4037
keywords:
- Флаги приоритета
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f4af04174ddb6c0ac459a6f7e6841e061b03c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068657"
---
# <a name="priority-flags"></a><span data-ttu-id="8f5d5-104">Флаги приоритета</span><span class="sxs-lookup"><span data-stu-id="8f5d5-104">Priority Flags</span></span>

<span data-ttu-id="8f5d5-105">Флаг приоритета открывает объект хранилища в режиме приоритета.</span><span class="sxs-lookup"><span data-stu-id="8f5d5-105">The priority flag opens a storage object in priority mode.</span></span> <span data-ttu-id="8f5d5-106">При открытии объекта приложение обычно работает из копии моментального снимка, так как другие приложения также могут использовать объект одновременно.</span><span class="sxs-lookup"><span data-stu-id="8f5d5-106">When it opens an object, an application usually works from a snapshot copy because other applications may also be using the object at the same time.</span></span> <span data-ttu-id="8f5d5-107">Однако при открытии объекта хранилища в режиме приоритета приложение имеет исключительные права на фиксацию изменений в объекте.</span><span class="sxs-lookup"><span data-stu-id="8f5d5-107">When opening a storage object in priority mode, however, the application has exclusive rights to commit changes to the object.</span></span>

<span data-ttu-id="8f5d5-108">Режим приоритета позволяет приложению считывать некоторые потоки из хранилища перед открытием объекта в режиме, требующем, чтобы система могла создать копию моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="8f5d5-108">Priority mode enables an application to read some streams from storage before opening the object in a mode that would require the system to make a snapshot copy.</span></span> <span data-ttu-id="8f5d5-109">Поскольку приложение имеет эксклюзивный доступ, ему не нужно создавать копию моментального снимка объекта.</span><span class="sxs-lookup"><span data-stu-id="8f5d5-109">Because the application has exclusive access, it does not have to make a snapshot copy of the object.</span></span> <span data-ttu-id="8f5d5-110">Когда приложение впоследствии открывает объект в режиме, где требуется копирование моментального снимка, приложение может исключить уже считанные из моментального снимка потоки, тем самым уменьшая издержки на открытие объекта.</span><span class="sxs-lookup"><span data-stu-id="8f5d5-110">When the application subsequently opens the object in a mode where a snapshot copy is required, the application can exclude the streams it has already read from the snapshot, thereby reducing the overhead of opening the object.</span></span>

<span data-ttu-id="8f5d5-111">Поскольку другие приложения не могут зафиксировать изменения в объекте, когда он открыт в режиме приоритета, приложения должны сохранить его в максимально короткие сроки.</span><span class="sxs-lookup"><span data-stu-id="8f5d5-111">Because other applications cannot commit changes to an object while it is open in priority mode, applications should keep the object in that mode for as short a time as possible.</span></span>

 

 




