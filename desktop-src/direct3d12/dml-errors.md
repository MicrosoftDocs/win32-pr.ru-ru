---
title: Обработка ошибок и удаление устройств в Директмл
description: В этом разделе описывается отладка Директмлного устройства и другие условия возникновения ошибок.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: b4567558b8b75685db16796e921f3daf35b849a1
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548972"
---
# <a name="handling-errors-and-device-removal-in-directml"></a><span data-ttu-id="998a1-103">Обработка ошибок и удаление устройств в Директмл</span><span class="sxs-lookup"><span data-stu-id="998a1-103">Handling errors and device-removal in DirectML</span></span>

## <a name="device-removal"></a><span data-ttu-id="998a1-104">Удаление устройства</span><span class="sxs-lookup"><span data-stu-id="998a1-104">Device-removal</span></span>

<span data-ttu-id="998a1-105">При возникновении неустранимой ошибки устройство Директмл может войти в состояние "удалено с устройства".</span><span class="sxs-lookup"><span data-stu-id="998a1-105">If an unrecoverable error occurs, the DirectML device may enter a "device-removed" state.</span></span> <span data-ttu-id="998a1-106">Неустранимые ошибки, вызывающие удаление устройства, включают недопустимое использование API (для методов, которые не возвращают [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)), ошибки драйвера, аппаратного сбоя или нехватки памяти (гонки).</span><span class="sxs-lookup"><span data-stu-id="998a1-106">Unrecoverable errors that cause device-removal include invalid API usage (for methods that don't return an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)), driver error, hardware fault, or out-of-memory (OOM) conditions.</span></span>

<span data-ttu-id="998a1-107">При удалении устройства Директмл все вызовы методов на устройстве и каждый объект, созданный этим устройством, становятся недоступными для операций.</span><span class="sxs-lookup"><span data-stu-id="998a1-107">When a DirectML device is removed, all method calls on the device, and every object created by that device, become no-ops.</span></span> <span data-ttu-id="998a1-108">Для методов, возвращающих [**значение HRESULT**](/windows/desktop/com/structure-of-com-error-codes), возвращается [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/direct3ddxgi/dxgi-error) код ошибки.</span><span class="sxs-lookup"><span data-stu-id="998a1-108">For methods that return an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes), a [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/direct3ddxgi/dxgi-error) error code is returned.</span></span> <span data-ttu-id="998a1-109">Вы можете использовать метод [ **идмлдевице:: жетдевицеремоведреасон**](/windows/desktop/api/directml/nf-directml-idmldevice-getdeviceremovedreason) , чтобы проверить, удалено ли устройство директмл, и получить более подробный код ошибки.</span><span class="sxs-lookup"><span data-stu-id="998a1-109">You can use the [**IDMLDevice::GetDeviceRemovedReason** method](/windows/desktop/api/directml/nf-directml-idmldevice-getdeviceremovedreason) to check whether the DirectML device has been removed, and to retrieve a more detailed error code.</span></span>

<span data-ttu-id="998a1-110">Восстановление после удаления устройства невозможно, за исключением выпуска затронутого устройства и всех его дочерних элементов, а затем повторного создания устройства Директмл с нуля.</span><span class="sxs-lookup"><span data-stu-id="998a1-110">You can't recover from device-removal except by releasing the affected device and all its children, then re-creating the DirectML device from scratch.</span></span>

<span data-ttu-id="998a1-111">Удаление устройства с базовым устройством Direct3D 12 также приводит к удалению устройства Директмл.</span><span class="sxs-lookup"><span data-stu-id="998a1-111">Device-removal of the underlying Direct3D 12 device also causes the DirectML device to be removed.</span></span> <span data-ttu-id="998a1-112">Однако обратное неверно.</span><span class="sxs-lookup"><span data-stu-id="998a1-112">However, the reverse is not true.</span></span> <span data-ttu-id="998a1-113">Удаление устройства Директмл может привести к тому, что базовое устройство Direct3D 12 не будет удалено.</span><span class="sxs-lookup"><span data-stu-id="998a1-113">DirectML device-removal may not necessarily cause the underlying Direct3D 12 device to become removed.</span></span>

## <a name="debugging-directml-device-removal-and-other-errors"></a><span data-ttu-id="998a1-114">Отладка устройства Директмл-удаление и другие ошибки</span><span class="sxs-lookup"><span data-stu-id="998a1-114">Debugging DirectML device-removal, and other errors</span></span>

<span data-ttu-id="998a1-115">Наиболее распространенной причиной ошибок Директмл является недопустимое использование API.</span><span class="sxs-lookup"><span data-stu-id="998a1-115">The most common cause of DirectML errors is invalid API usage.</span></span> <span data-ttu-id="998a1-116">Недопустимое использование API может привести к **E_INVALIDARG** коду ошибки HRESULT или в результате удаления устройства.</span><span class="sxs-lookup"><span data-stu-id="998a1-116">Invalid API usage might result in an **E_INVALIDARG** HRESULT error code, or it might result in device-removal.</span></span>

<span data-ttu-id="998a1-117">Мы настоятельно рекомендуем включить [уровень отладки директмл](dml-debug-layer.md) во время разработки, чтобы перехватить и отладить такие ошибки.</span><span class="sxs-lookup"><span data-stu-id="998a1-117">We strongly recommend that you enable the [DirectML debug layer](dml-debug-layer.md) during your development, in order to catch and debug such errors.</span></span> <span data-ttu-id="998a1-118">Уровень отладки Директмл выполняет расширенную проверку параметров метода и использования API, а также выдает отладочные сообщения отладки, которые помогут вам выполнить отладку.</span><span class="sxs-lookup"><span data-stu-id="998a1-118">The DirectML debug layer performs extensive validation of method parameters and API usage, and it will emit debug output messages to help you debug.</span></span>

## <a name="see-also"></a><span data-ttu-id="998a1-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="998a1-119">See also</span></span>

* [<span data-ttu-id="998a1-120">Использование слоя отладки Директмл</span><span class="sxs-lookup"><span data-stu-id="998a1-120">Using the DirectML debug layer</span></span>](dml-debug-layer.md)
