---
title: Создание дисков с несколькими сеансами
description: IMAPI способен создавать диски данных с несколькими сеансами. При создании диска с несколькими сеансами необходимо учитывать несколько моментов.
ms.assetid: 02405a32-53d5-4618-bfa0-c9a9f5e3c51b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc41dba861ce29bd3d3e25e33ba0ba5ab5bf38a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253113"
---
# <a name="creating-discs-with-multiple-sessions"></a><span data-ttu-id="e02bf-104">Создание дисков с несколькими сеансами</span><span class="sxs-lookup"><span data-stu-id="e02bf-104">Creating Discs with Multiple Sessions</span></span>

<span data-ttu-id="e02bf-105">IMAPI способен создавать диски данных с несколькими сеансами.</span><span class="sxs-lookup"><span data-stu-id="e02bf-105">IMAPI is capable of creating multi-session data discs.</span></span> <span data-ttu-id="e02bf-106">При создании диска с несколькими сеансами необходимо учитывать несколько моментов.</span><span class="sxs-lookup"><span data-stu-id="e02bf-106">There are a few considerations to be aware of when creating a multi-session disc.</span></span>

<span data-ttu-id="e02bf-107">Метод [**идискмастер:: сетактиведискрекордер**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder) определяет, есть ли на активном диске диск с несколькими СЕАНСАми IMAPI для настройки.</span><span class="sxs-lookup"><span data-stu-id="e02bf-107">The [**IDiscMaster::SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder) method determines whether there is an IMAPI multi-session disc in the active drive upon setting.</span></span> <span data-ttu-id="e02bf-108">В этом случае IMAPI переходит в режим многосеансовой связи автоматически.</span><span class="sxs-lookup"><span data-stu-id="e02bf-108">If so, IMAPI goes into multi-session mode automatically.</span></span> <span data-ttu-id="e02bf-109">Использование [**клеарформатконтент**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) после установки режима с несколькими сеансами приводит к тому, что IMAPI возвращается в односеансовый режим.</span><span class="sxs-lookup"><span data-stu-id="e02bf-109">Using [**ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) after multi-session mode has been established causes IMAPI to return to single-session mode.</span></span> <span data-ttu-id="e02bf-110">Это означает, что для записи [**рекорддиск**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) требуется пустой диск.</span><span class="sxs-lookup"><span data-stu-id="e02bf-110">This means that a blank disc is required for a [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) burn.</span></span> <span data-ttu-id="e02bf-111">Если диск находится в режиме с несколькими сеансами, то один и тот же диск должен находиться в активном средстве записи или возвращен код ошибки IMAPI \_ E \_ вронгдиск.</span><span class="sxs-lookup"><span data-stu-id="e02bf-111">If the disc is in multi-session mode, the same disc must be in the active recorder or an error code of IMAPI\_E\_WRONGDISC will be returned.</span></span>

<span data-ttu-id="e02bf-112">Выбор средства записи в формате Жолиет приводит к тому, что IMAPI считывает данные с установленного на данный момент диска. Если диск является предыдущим диском IMAPI Жолиет, в котором есть место для другого сеанса, то IMAPI автоматически переводит себя в режим многосеансового режима.</span><span class="sxs-lookup"><span data-stu-id="e02bf-112">Selecting a recorder while in Joliet format causes IMAPI to read information from the currently installed disc. If the disc is a previous IMAPI Joliet disc that has space for another session, IMAPI automatically sets itself to multi-session mode.</span></span> <span data-ttu-id="e02bf-113">Этот диск должен присутствовать в активном средстве записи при вызове [**рекорддиск**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc).</span><span class="sxs-lookup"><span data-stu-id="e02bf-113">This disc must be present in the active recorder when calling [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc).</span></span>

<span data-ttu-id="e02bf-114">Для закрытия первого сеанса на диске требуется 21 МБ.</span><span class="sxs-lookup"><span data-stu-id="e02bf-114">Closing the first session on a disc requires 21 MB.</span></span> <span data-ttu-id="e02bf-115">Для каждого дополнительного сеанса требуется около 11 МБ.</span><span class="sxs-lookup"><span data-stu-id="e02bf-115">Each additional session requires 11 MB to close.</span></span>

 

 




