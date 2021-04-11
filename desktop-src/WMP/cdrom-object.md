---
title: Объект CDROM
description: Объект CDROM предоставляет способ доступа к компакт-диску или DVD-диску на его диске.
ms.assetid: 9045b130-3e08-4880-a4e7-79b704c4c1f9
keywords:
- Проигрыватель Windows Media объект CDROM
topic_type:
- apiref
api_name:
- Cdrom Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17c2de88749b4dd4a0ab756b77866c16e8878486
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333192"
---
# <a name="cdrom-object"></a><span data-ttu-id="0299b-104">Объект CDROM</span><span class="sxs-lookup"><span data-stu-id="0299b-104">Cdrom Object</span></span>

<span data-ttu-id="0299b-105">Объект **CDROM** предоставляет способ доступа к компакт-диску или DVD-диску на его диске.</span><span class="sxs-lookup"><span data-stu-id="0299b-105">The **Cdrom** object provides a way to access a CD or DVD in its drive.</span></span>

<span data-ttu-id="0299b-106">Объект **CDROM** поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0299b-106">The **Cdrom** object supports the following properties.</span></span>



| <span data-ttu-id="0299b-107">Свойство</span><span class="sxs-lookup"><span data-stu-id="0299b-107">Property</span></span>                                   | <span data-ttu-id="0299b-108">Описание</span><span class="sxs-lookup"><span data-stu-id="0299b-108">Description</span></span>                                                                                                                                             |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0299b-109">дривеспеЦифиер</span><span class="sxs-lookup"><span data-stu-id="0299b-109">driveSpecifier</span></span>](cdrom-drivespecifier.md) | <span data-ttu-id="0299b-110">Возвращает букву компакт-диска или DVD-дисковода.</span><span class="sxs-lookup"><span data-stu-id="0299b-110">Retrieves the CD or DVD drive letter.</span></span>                                                                                                                   |
| [<span data-ttu-id="0299b-111">список воспроизведения</span><span class="sxs-lookup"><span data-stu-id="0299b-111">playlist</span></span>](cdrom-playlist.md)             | <span data-ttu-id="0299b-112">Извлекает объект [списка воспроизведения](playlist-object.md) , который представляет дорожки на компакт-диске в данный момент в ДИСКОВОДе компакт-дисков или записи заголовка корневого уровня для DVD.</span><span class="sxs-lookup"><span data-stu-id="0299b-112">Retrieves a [Playlist](playlist-object.md) object representing the tracks on the CD currently in the CD drive or the root-level title entries for DVD.</span></span> |



 

<span data-ttu-id="0299b-113">Объект **CDROM** поддерживает следующий метод.</span><span class="sxs-lookup"><span data-stu-id="0299b-113">The **Cdrom** object supports the following method.</span></span>



| <span data-ttu-id="0299b-114">Метод</span><span class="sxs-lookup"><span data-stu-id="0299b-114">Method</span></span>                   | <span data-ttu-id="0299b-115">Описание</span><span class="sxs-lookup"><span data-stu-id="0299b-115">Description</span></span>                          |
|--------------------------|--------------------------------------|
| [<span data-ttu-id="0299b-116">выдвинут</span><span class="sxs-lookup"><span data-stu-id="0299b-116">eject</span></span>](cdrom-eject.md) | <span data-ttu-id="0299b-117">Извлекает компакт-диск или DVD-диск из накопителя.</span><span class="sxs-lookup"><span data-stu-id="0299b-117">Ejects the CD or DVD from the drive.</span></span> |



 

<span data-ttu-id="0299b-118">Доступ к объекту **CDROM** осуществляется с помощью следующего метода.</span><span class="sxs-lookup"><span data-stu-id="0299b-118">The **Cdrom** object is accessed through the following method.</span></span>



| <span data-ttu-id="0299b-119">Объект</span><span class="sxs-lookup"><span data-stu-id="0299b-119">Object</span></span>                                        | <span data-ttu-id="0299b-120">Метод</span><span class="sxs-lookup"><span data-stu-id="0299b-120">Method</span></span>                           |
|-----------------------------------------------|----------------------------------|
| [<span data-ttu-id="0299b-121">кдромколлектион</span><span class="sxs-lookup"><span data-stu-id="0299b-121">CdromCollection</span></span>](cdromcollection-object.md) | [<span data-ttu-id="0299b-122">Item</span><span class="sxs-lookup"><span data-stu-id="0299b-122">item</span></span>](cdromcollection-item.md) |



 

<span data-ttu-id="0299b-123">В целях иллюстрации в разделах синтаксиса Reference используется проигрыватель. Кдромколлектион. Item (*индекс*).</span><span class="sxs-lookup"><span data-stu-id="0299b-123">For purposes of illustration, player.cdromCollection.item(*index*) is used in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="0299b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0299b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0299b-125">**Справочник по объектной модели для создания сценариев**</span><span class="sxs-lookup"><span data-stu-id="0299b-125">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




