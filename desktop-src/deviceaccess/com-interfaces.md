---
title: COM-интерфейсы — доступ к устройствам
description: Интерфейсы модели COM в API доступа к устройству.
ms.assetid: 96F532B7-5CF9-4341-932B-7F8BEDA9551F
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 07abbfd15f8383bbbd9cd9d1f5fc4c9fb1f42b9e
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "104070817"
---
# <a name="com-interfaces---device-access"></a><span data-ttu-id="65437-103">COM-интерфейсы — доступ к устройствам</span><span class="sxs-lookup"><span data-stu-id="65437-103">COM Interfaces - Device Access</span></span>

<span data-ttu-id="65437-104">Интерфейсы модели COM в API доступа к устройству.</span><span class="sxs-lookup"><span data-stu-id="65437-104">Component Object Model (COM)interfaces in the Device Access API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="65437-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="65437-105">In this section</span></span>

| <span data-ttu-id="65437-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="65437-106">Topic</span></span> | <span data-ttu-id="65437-107">Описание</span><span class="sxs-lookup"><span data-stu-id="65437-107">Description</span></span> |
|---|---|
| [<span data-ttu-id="65437-108">**икреатедевицеакцессасинк**</span><span class="sxs-lookup"><span data-stu-id="65437-108">**ICreateDeviceAccessAsync**</span></span>](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync)<br/> | <span data-ttu-id="65437-109">Интерфейс [**икреатедевицеакцессасинк**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) возвращается из вызова креатедевицеакцессинстанце.</span><span class="sxs-lookup"><span data-stu-id="65437-109">The [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) interface is returned from a call to CreateDeviceAccessInstance.</span></span> <span data-ttu-id="65437-110">Он позволяет вызывающему объекту управлять операцией привязки к экземпляру устройства, чтобы получить другой интерфейс, который можно использовать для взаимодействия с этим устройством.</span><span class="sxs-lookup"><span data-stu-id="65437-110">It enables the caller to control the operation of binding to an instance of a device in order to retrieve another interface that can be used to interact with that device.</span></span><br/> |
| [<span data-ttu-id="65437-111">**идевицеиоконтрол**</span><span class="sxs-lookup"><span data-stu-id="65437-111">**IDeviceIoControl**</span></span>](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol)<br/> | <span data-ttu-id="65437-112">Отправляет управляющий код в драйвер устройства. Это действие заставляет устройство выполнить соответствующую операцию.</span><span class="sxs-lookup"><span data-stu-id="65437-112">Sends a control code to a device driver.This action causes the device to perform the corresponding operation.</span></span> <br/> |
| [<span data-ttu-id="65437-113">**идевицерекуесткомплетионкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="65437-113">**IDeviceRequestCompletionCallback**</span></span>](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback)<br/> | <span data-ttu-id="65437-114">Предоставляет метод для управления завершением вызовов метода [**девицеиоконтроласинк**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync).</span><span class="sxs-lookup"><span data-stu-id="65437-114">Provides a method to handle the completion of calls to the [**DeviceIoControlAsync**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync)method.</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="65437-115">См. также</span><span class="sxs-lookup"><span data-stu-id="65437-115">Related topics</span></span>

<span data-ttu-id="65437-116">[Пример пользовательского доступа к драйверу](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [приложения для устройств UWP для внутренних устройств](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [центр разработки оборудования](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="65437-116">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>
