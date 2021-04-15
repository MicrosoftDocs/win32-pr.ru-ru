---
title: Settings. baseURL
description: Свойство baseURL указывает или получает базовый URL-адрес, используемый для разрешения относительных путей с помощью команд сценария URL-адреса, внедренных в элементы мультимедиа.
ms.assetid: bb2db144-6d1e-4ed6-baed-dc5dbff44aa0
keywords:
- Проигрыватель Windows Media Settings. baseURL
topic_type:
- apiref
api_name:
- Settings.baseURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed77d90c8ffadc4dd8da0951f7e6a477db3f9de3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647989"
---
# <a name="settingsbaseurl"></a><span data-ttu-id="297ae-104">Settings. baseURL</span><span class="sxs-lookup"><span data-stu-id="297ae-104">Settings.baseURL</span></span>

<span data-ttu-id="297ae-105">Свойство **baseURL** указывает или получает базовый URL-адрес, используемый для разрешения относительных путей с помощью команд сценария URL-адреса, внедренных в элементы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="297ae-105">The **baseURL** property specifies or retrieves the base URL used for relative path resolution with URL script commands that are embedded in media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="297ae-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="297ae-106">Syntax</span></span>

<span data-ttu-id="297ae-107">Player. Settings. baseURL</span><span class="sxs-lookup"><span data-stu-id="297ae-107">player.settings.baseURL</span></span>

## <a name="possible-values"></a><span data-ttu-id="297ae-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="297ae-108">Possible Values</span></span>

<span data-ttu-id="297ae-109">Это свойство является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="297ae-109">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="297ae-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="297ae-110">Remarks</span></span>

<span data-ttu-id="297ae-111">Это свойство указывает базовый URL-адрес HTTP, который передается событием **команду скрипта** в качестве параметра команды.</span><span class="sxs-lookup"><span data-stu-id="297ae-111">This property specifies the base HTTP URL that is passed as the command parameter by the **ScriptCommand** event.</span></span> <span data-ttu-id="297ae-112">Базовый URL-адрес объединяется с относительным URL-адресом следующим образом:</span><span class="sxs-lookup"><span data-stu-id="297ae-112">The base URL is concatenated with the relative URL as follows:</span></span>

1.  <span data-ttu-id="297ae-113">В значение свойства **baseURL** добавляется Замыкающая косая черта (/).</span><span class="sxs-lookup"><span data-stu-id="297ae-113">A trailing forward slash (/) is added to the value of the **baseURL** property.</span></span>
2.  <span data-ttu-id="297ae-114">Начальная точка, обратная косая черта или косая черта (., \\ и/) удаляются из относительного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="297ae-114">A leading period, backward slash, or forward slash (., \\, and /) are deleted from the relative URL.</span></span>
3.  <span data-ttu-id="297ae-115">Относительный URL-адрес добавляется в конец базового URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="297ae-115">The relative URL is added to the end of the base URL.</span></span>
4.  <span data-ttu-id="297ae-116">Все косые черты в результирующем полном URL-адресе указываются в том же направлении (преобразованном в прямую или обратную косую черту) в зависимости от направления первой косой черты, обнаруженной в новом URL-адресе.</span><span class="sxs-lookup"><span data-stu-id="297ae-116">All slashes in the resulting fully qualified URL are pointed in the same direction (converted to forward or backward slashes) based on the direction of the first slash character encountered in the new URL.</span></span>

<span data-ttu-id="297ae-117">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="297ae-117">**Note**</span></span>

<span data-ttu-id="297ae-118">Элемент управления "проигрыватель" не поддерживает использование двух точек (..) в относительном URL-адресе для указания родителя текущего расположения.</span><span class="sxs-lookup"><span data-stu-id="297ae-118">The player control does not support the use of two periods (..) in the relative URL to indicate the parent of the current location.</span></span>

<span data-ttu-id="297ae-119">**Проигрыватель Windows Media 10 Mobile**: это свойство доступно только для чтения и всегда возвращает пустую строку.</span><span class="sxs-lookup"><span data-stu-id="297ae-119">**Windows Media Player 10 Mobile**: This property is read-only, and always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="297ae-120">Требования</span><span class="sxs-lookup"><span data-stu-id="297ae-120">Requirements</span></span>



| <span data-ttu-id="297ae-121">Требование</span><span class="sxs-lookup"><span data-stu-id="297ae-121">Requirement</span></span> | <span data-ttu-id="297ae-122">Значение</span><span class="sxs-lookup"><span data-stu-id="297ae-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="297ae-123">Версия</span><span class="sxs-lookup"><span data-stu-id="297ae-123">Version</span></span><br/> | <span data-ttu-id="297ae-124">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="297ae-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="297ae-125">DLL</span><span class="sxs-lookup"><span data-stu-id="297ae-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="297ae-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="297ae-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="297ae-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="297ae-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="297ae-128">**Событие Player. команду скрипта**</span><span class="sxs-lookup"><span data-stu-id="297ae-128">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="297ae-129">**Объект параметров**</span><span class="sxs-lookup"><span data-stu-id="297ae-129">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





