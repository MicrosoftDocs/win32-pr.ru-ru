---
description: Для сетевого DDE используются следующие функции.
ms.assetid: 5fd61759-1792-4db0-9ad4-adf112294b9c
title: Сетевые функции DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16e5ae6a38ec6324cf33b4f9c4ffc1af44473699
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693772"
---
# <a name="network-dde-functions"></a><span data-ttu-id="a9842-103">Сетевые функции DDE</span><span class="sxs-lookup"><span data-stu-id="a9842-103">Network DDE Functions</span></span>

<span data-ttu-id="a9842-104">\[Сетевой DDE больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a9842-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="a9842-105">Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают НДДЕ \_ не \_ реализован.\]</span><span class="sxs-lookup"><span data-stu-id="a9842-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="a9842-106">Для сетевого DDE используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="a9842-106">The following functions are used with network DDE.</span></span>



| <span data-ttu-id="a9842-107">Функция</span><span class="sxs-lookup"><span data-stu-id="a9842-107">Function</span></span>                                                   | <span data-ttu-id="a9842-108">Описание</span><span class="sxs-lookup"><span data-stu-id="a9842-108">Description</span></span>                                                                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9842-109">**нддежетеррорстринг**</span><span class="sxs-lookup"><span data-stu-id="a9842-109">**NDdeGetErrorString**</span></span>](nddegeterrorstring.md)           | <span data-ttu-id="a9842-110">Преобразует код ошибки, возвращенный сетевой функцией DDE, в строку ошибки, объясняющую возвращенный код ошибки.</span><span class="sxs-lookup"><span data-stu-id="a9842-110">Converts an error code returned by a network DDE function into an error string that explains the returned error code.</span></span> |
| [<span data-ttu-id="a9842-111">**нддежетшаресекурити**</span><span class="sxs-lookup"><span data-stu-id="a9842-111">**NDdeGetShareSecurity**</span></span>](nddegetsharesecurity.md)       | <span data-ttu-id="a9842-112">Извлекает дескриптор безопасности, связанный с общим ресурсом DDE.</span><span class="sxs-lookup"><span data-stu-id="a9842-112">Retrieves the security descriptor associated with the DDE share.</span></span>                                                      |
| [<span data-ttu-id="a9842-113">**нддежеттрустедшаре**</span><span class="sxs-lookup"><span data-stu-id="a9842-113">**NDdeGetTrustedShare**</span></span>](nddegettrustedshare.md)         | <span data-ttu-id="a9842-114">Извлекает параметры, связанные с общим ресурсом DDE, который находится в списке доверенных общих ресурсов пользователя сервера.</span><span class="sxs-lookup"><span data-stu-id="a9842-114">Retrieves the options associated with a DDE share that is in the server user's list of trusted shares.</span></span>                |
| [<span data-ttu-id="a9842-115">**нддеисвалидапптопиклист**</span><span class="sxs-lookup"><span data-stu-id="a9842-115">**NDdeIsValidAppTopicList**</span></span>](nddeisvalidapptopiclist.md) | <span data-ttu-id="a9842-116">Определяет, использует ли строка приложения и раздела ("*AppName* \| *топикнаме*") правильный синтаксис.</span><span class="sxs-lookup"><span data-stu-id="a9842-116">Determines whether an application and topic string ("*AppName*\|*TopicName*") uses the proper syntax.</span></span>                 |
| [<span data-ttu-id="a9842-117">**нддеисвалидшаренаме**</span><span class="sxs-lookup"><span data-stu-id="a9842-117">**NDdeIsValidShareName**</span></span>](nddeisvalidsharename.md)       | <span data-ttu-id="a9842-118">Определяет, использует ли имя общего ресурса правильный синтаксис.</span><span class="sxs-lookup"><span data-stu-id="a9842-118">Determines whether a share name uses the proper syntax.</span></span>                                                               |
| [<span data-ttu-id="a9842-119">**нддесетшаресекурити**</span><span class="sxs-lookup"><span data-stu-id="a9842-119">**NDdeSetShareSecurity**</span></span>](nddesetsharesecurity.md)       | <span data-ttu-id="a9842-120">Задает дескриптор безопасности, связанный с общим ресурсом DDE.</span><span class="sxs-lookup"><span data-stu-id="a9842-120">Sets the security descriptor associated with the DDE share.</span></span>                                                           |
| [<span data-ttu-id="a9842-121">**нддесеттрустедшаре**</span><span class="sxs-lookup"><span data-stu-id="a9842-121">**NDdeSetTrustedShare**</span></span>](nddesettrustedshare.md)         | <span data-ttu-id="a9842-122">Предоставляет указанное состояние доверия общего ресурса DDE в контексте текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="a9842-122">Grants the specified DDE share trusted status within the current user's context.</span></span>                                      |
| [<span data-ttu-id="a9842-123">**нддешареадд**</span><span class="sxs-lookup"><span data-stu-id="a9842-123">**NDdeShareAdd**</span></span>](nddeshareadd.md)                       | <span data-ttu-id="a9842-124">Создает и добавляет новый общий ресурс DDE в диспетчер общей базы данных DDE (DSDM).</span><span class="sxs-lookup"><span data-stu-id="a9842-124">Creates and adds a new DDE share to the DDE share database manager (DSDM).</span></span>                                            |
| [<span data-ttu-id="a9842-125">**нддешаредел**</span><span class="sxs-lookup"><span data-stu-id="a9842-125">**NDdeShareDel**</span></span>](nddesharedel.md)                       | <span data-ttu-id="a9842-126">Удаляет общую папку DDE из DSDM.</span><span class="sxs-lookup"><span data-stu-id="a9842-126">Deletes a DDE share from the DSDM.</span></span>                                                                                    |
| [<span data-ttu-id="a9842-127">**нддешаринум**</span><span class="sxs-lookup"><span data-stu-id="a9842-127">**NDdeShareEnum**</span></span>](nddeshareenum.md)                     | <span data-ttu-id="a9842-128">Возвращает список доступных общих ресурсов DDE.</span><span class="sxs-lookup"><span data-stu-id="a9842-128">Retrieves the list of available DDE shares.</span></span>                                                                           |
| [<span data-ttu-id="a9842-129">**нддешарежетинфо**</span><span class="sxs-lookup"><span data-stu-id="a9842-129">**NDdeShareGetInfo**</span></span>](nddesharegetinfo.md)               | <span data-ttu-id="a9842-130">Извлекает сведения об общем ресурсе DDE.</span><span class="sxs-lookup"><span data-stu-id="a9842-130">Retrieves DDE share information.</span></span>                                                                                      |
| [<span data-ttu-id="a9842-131">**нддешаресетинфо**</span><span class="sxs-lookup"><span data-stu-id="a9842-131">**NDdeShareSetInfo**</span></span>](nddesharesetinfo.md)               | <span data-ttu-id="a9842-132">Задает общие сведения об общем ресурсе DDE.</span><span class="sxs-lookup"><span data-stu-id="a9842-132">Sets DDE share information.</span></span>                                                                                           |
| [<span data-ttu-id="a9842-133">**нддетрустедшаринум**</span><span class="sxs-lookup"><span data-stu-id="a9842-133">**NDdeTrustedShareEnum**</span></span>](nddetrustedshareenum.md)       | <span data-ttu-id="a9842-134">Возвращает имена всех общих сетевых ресурсов DDE, которые являются доверенными в контексте вызывающего процесса.</span><span class="sxs-lookup"><span data-stu-id="a9842-134">Retrieves the names of all network DDE shares that are trusted in the context of the calling process.</span></span>                 |



 

 

 



