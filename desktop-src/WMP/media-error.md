---
title: Media. Error
description: Свойство Error извлекает объект Ерроритем, если у элемента мультимедиа есть условие ошибки.
ms.assetid: cd572688-12f9-4615-8f22-9442d615a2b6
keywords:
- Media. Error Windows Media Player
topic_type:
- apiref
api_name:
- Media.error
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5845252c817a424b0cbe414612fde47ed8b57328
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651775"
---
# <a name="mediaerror"></a><span data-ttu-id="ee34d-104">Media. Error</span><span class="sxs-lookup"><span data-stu-id="ee34d-104">Media.error</span></span>

<span data-ttu-id="ee34d-105">Свойство **Error** извлекает объект **ерроритем** , если у элемента мультимедиа есть условие ошибки.</span><span class="sxs-lookup"><span data-stu-id="ee34d-105">The **error** property retrieves an **ErrorItem** object if the media item has an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee34d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee34d-106">Syntax</span></span>

<span data-ttu-id="ee34d-107">*проигрыватель*. *куррентмедиа*. **Ошибка при**</span><span class="sxs-lookup"><span data-stu-id="ee34d-107">*player*.*currentMedia*.**error**</span></span>

## <a name="possible-values"></a><span data-ttu-id="ee34d-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="ee34d-108">Possible Values</span></span>

<span data-ttu-id="ee34d-109">Это свойство является объектом **ерроритем** , предназначенным только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ee34d-109">This property is a read-only **ErrorItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee34d-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ee34d-110">Remarks</span></span>

<span data-ttu-id="ee34d-111">Если не удается воспроизвести элемент мультимедиа, это свойство получает объект **ерроритем** , содержащий сведения о возникшей проблеме.</span><span class="sxs-lookup"><span data-stu-id="ee34d-111">If the media item cannot be played, this property retrieves an **ErrorItem** object that contains information about the problem encountered.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee34d-112">Требования</span><span class="sxs-lookup"><span data-stu-id="ee34d-112">Requirements</span></span>



| <span data-ttu-id="ee34d-113">Требование</span><span class="sxs-lookup"><span data-stu-id="ee34d-113">Requirement</span></span> | <span data-ttu-id="ee34d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="ee34d-114">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ee34d-115">Версия</span><span class="sxs-lookup"><span data-stu-id="ee34d-115">Version</span></span><br/> | <span data-ttu-id="ee34d-116">Проигрыватель Windows Media для Windows XP или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ee34d-116">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="ee34d-117">DLL</span><span class="sxs-lookup"><span data-stu-id="ee34d-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="ee34d-118"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee34d-118"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee34d-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee34d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee34d-120">**Объект Ерроритем**</span><span class="sxs-lookup"><span data-stu-id="ee34d-120">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> <dt>

[<span data-ttu-id="ee34d-121">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="ee34d-121">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 





