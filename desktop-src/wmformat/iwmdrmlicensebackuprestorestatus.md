---
title: Интерфейс Ивмдрмлиценсебаккупресторестатус
description: Интерфейс Ивмдрмлиценсебаккупресторестатус предоставляет метод для получения подробных сведений о состоянии операции резервного копирования или восстановления лицензий. Этот интерфейс доставляется с событиями хода выполнения, созданными во время операций резервного копирования и восстановления лицензий.
ms.assetid: fbcd059f-13d9-4edb-8946-b55c9da6dca4
keywords:
- Формат Windows Media в интерфейсе Ивмдрмлиценсебаккупресторестатус
- Ивмдрмлиценсебаккупресторестатус интерфейса Windows Media Format, описание
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9db5d95daab78a506a3cc994fb9dd22153d0907
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338620"
---
# <a name="iwmdrmlicensebackuprestorestatus-interface"></a><span data-ttu-id="403b8-105">Интерфейс Ивмдрмлиценсебаккупресторестатус</span><span class="sxs-lookup"><span data-stu-id="403b8-105">IWMDRMLicenseBackupRestoreStatus interface</span></span>

<span data-ttu-id="403b8-106">Интерфейс **ивмдрмлиценсебаккупресторестатус** предоставляет метод для получения подробных сведений о состоянии операции резервного копирования или восстановления лицензий.</span><span class="sxs-lookup"><span data-stu-id="403b8-106">The **IWMDRMLicenseBackupRestoreStatus** interface provides a method to retrieve detailed status information about a license backup or restore operation.</span></span>

<span data-ttu-id="403b8-107">Этот интерфейс доставляется с событиями хода выполнения, созданными во время операций резервного копирования и восстановления лицензий.</span><span class="sxs-lookup"><span data-stu-id="403b8-107">This interface is delivered with progress events generated during license backup and restore operations.</span></span> <span data-ttu-id="403b8-108">Во время резервного копирования лицензий создаются несколько событий **мевмдрмлиценсебаккуппрогресс** , каждый из которых имеет сопутствующий экземпляр этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="403b8-108">Several **MEWMDRMLicenseBackupProgress** events are generated during license backup, each of which has an accompanying instance of this interface.</span></span> <span data-ttu-id="403b8-109">То же самое относится к событиям **мевмдрмлиценсересторепрогресс** , которые создаются во время восстановления лицензии.</span><span class="sxs-lookup"><span data-stu-id="403b8-109">The same is true of **MEWMDRMLicenseRestoreProgress** events, which are generated during license restoration.</span></span>

<span data-ttu-id="403b8-110">Чтобы получить указатель на экземпляр интерфейса **ивмдрмлиценсебаккупресторестатус** , необходимо сначала вызвать метод **Имфмедиаевент:: GetValue** события Progress.</span><span class="sxs-lookup"><span data-stu-id="403b8-110">To retrieve a pointer to an instance of the **IWMDRMLicenseBackupRestoreStatus** interface, you must first call the **IMFMediaEvent::GetValue** method of the progress event.</span></span> <span data-ttu-id="403b8-111">Значение, получаемое из события, является указателем на интерфейс **IUnknown** объекта, реализующего интерфейс **ивмдрмлиценсебаккупресторестатус** .</span><span class="sxs-lookup"><span data-stu-id="403b8-111">The value you retrieve from the event is a pointer to the **IUnknown** interface of the object that implements the **IWMDRMLicenseBackupRestoreStatus** interface.</span></span>

## <a name="members"></a><span data-ttu-id="403b8-112">Элементы</span><span class="sxs-lookup"><span data-stu-id="403b8-112">Members</span></span>

<span data-ttu-id="403b8-113">Интерфейс **ивмдрмлиценсебаккупресторестатус** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="403b8-113">The **IWMDRMLicenseBackupRestoreStatus** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="403b8-114">**Ивмдрмлиценсебаккупресторестатус** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="403b8-114">**IWMDRMLicenseBackupRestoreStatus** also has these types of members:</span></span>

-   [<span data-ttu-id="403b8-115">Методы</span><span class="sxs-lookup"><span data-stu-id="403b8-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="403b8-116">Методы</span><span class="sxs-lookup"><span data-stu-id="403b8-116">Methods</span></span>

<span data-ttu-id="403b8-117">Интерфейс **ивмдрмлиценсебаккупресторестатус** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="403b8-117">The **IWMDRMLicenseBackupRestoreStatus** interface has these methods.</span></span>



| <span data-ttu-id="403b8-118">Метод</span><span class="sxs-lookup"><span data-stu-id="403b8-118">Method</span></span>                                                          | <span data-ttu-id="403b8-119">Описание</span><span class="sxs-lookup"><span data-stu-id="403b8-119">Description</span></span>                                                                                   |
|:----------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="403b8-120">**GetStatus**</span><span class="sxs-lookup"><span data-stu-id="403b8-120">**GetStatus**</span></span>](iwmdrmlicensebackuprestorestatus-getstatus.md) | <span data-ttu-id="403b8-121">Получает подробные сведения о состоянии операции резервного копирования или восстановления лицензий.</span><span class="sxs-lookup"><span data-stu-id="403b8-121">Retrieves detailed status information about a license backup or restore operation.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="403b8-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="403b8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="403b8-123">**Интерфейсы**</span><span class="sxs-lookup"><span data-stu-id="403b8-123">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

