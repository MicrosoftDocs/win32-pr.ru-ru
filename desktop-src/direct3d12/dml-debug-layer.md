---
title: Использование слоя отладки Директмл
description: Уровень отладки Директмл — это дополнительный компонент времени разработки, который помогает в отладке кода Директмл.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: f885595e5cc3b3890d208875fb92e47e0dc5e337
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "104548973"
---
# <a name="using-the-directml-debug-layer"></a><span data-ttu-id="835e5-103">Использование слоя отладки Директмл</span><span class="sxs-lookup"><span data-stu-id="835e5-103">Using the DirectML debug layer</span></span>

<span data-ttu-id="835e5-104">Уровень отладки Директмл — это дополнительный компонент времени разработки, который помогает в отладке кода Директмл.</span><span class="sxs-lookup"><span data-stu-id="835e5-104">The DirectML debug layer is an optional development-time component that helps you in debugging your DirectML code.</span></span> <span data-ttu-id="835e5-105">Слой отладки является частью отдельного пакета графических средств, распространяемого как [функция по требованию](/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (FOD).</span><span class="sxs-lookup"><span data-stu-id="835e5-105">The debug layer is part of a separate Graphics Tools package, distributed as a [Feature-on-Demand](/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (FOD).</span></span> <span data-ttu-id="835e5-106">Для использования слоя отладки в системе должны быть установлены средства Graphics Tools FOD.</span><span class="sxs-lookup"><span data-stu-id="835e5-106">The Graphics Tools FOD must be installed on your system in order to use the debug layer.</span></span>

<span data-ttu-id="835e5-107">Мы настоятельно рекомендуем включить уровень отладки при разработке приложений с помощью Директмл, так как он может предоставить ценную информацию в случае недопустимого использования API.</span><span class="sxs-lookup"><span data-stu-id="835e5-107">We highly recommended that you enable the debug layer while developing applications using DirectML, because it can provide invaluable information in the event of invalid API usage.</span></span>

## <a name="installing-the-directml-debug-layer"></a><span data-ttu-id="835e5-108">Установка слоя отладки Директмл</span><span class="sxs-lookup"><span data-stu-id="835e5-108">Installing the DirectML debug layer</span></span>

<span data-ttu-id="835e5-109">Чтобы установить дополнительный пакет по запросу для графических инструментов (FOD), выполните следующую команду в командной строке администратора PowerShell.</span><span class="sxs-lookup"><span data-stu-id="835e5-109">To install the optional Graphics Tools feature-on-demand (FOD) package, run the following command from an administrator Powershell prompt.</span></span>

```powershell
Add-WindowsCapability -Online -Name "Tools.Graphics.DirectX~~~~0.0.1.0"
```

<span data-ttu-id="835e5-110">Кроме того, пакет средств для обработки графики можно установить с помощью параметров Windows 10.</span><span class="sxs-lookup"><span data-stu-id="835e5-110">Alternatively, you can install the Graphics Tools package from within Windows 10 Settings.</span></span> <span data-ttu-id="835e5-111">Перейдите к разделу **Параметры**  >  **приложения приложения**  >  **& функции**  >  **Дополнительные функции**  >  **Добавить компонент** > затем выберите **графические инструменты**.</span><span class="sxs-lookup"><span data-stu-id="835e5-111">Navigate to **Settings** > **Apps** > **Apps & features** > **Optional features** > **Add a feature** > then select **Graphics Tools**.</span></span>

## <a name="enabling-the-directml-debug-layer"></a><span data-ttu-id="835e5-112">Включение слоя отладки Директмл</span><span class="sxs-lookup"><span data-stu-id="835e5-112">Enabling the DirectML debug layer</span></span>

<span data-ttu-id="835e5-113">После установки пакета средств для обработки графики можно включить уровень отладки Директмл, указав  [**DML_CREATE_DEVICE_FLAG_DEBUG**](/windows/win32/api/directml/ne-directml-dml_create_device_flags) при вызове [**дмлкреатедевице**](/windows/win32/api/directml/nf-directml-dmlcreatedevice).</span><span class="sxs-lookup"><span data-stu-id="835e5-113">Once the Graphics Tools package is installed, you can enable the DirectML debug layer by supplying  [**DML_CREATE_DEVICE_FLAG_DEBUG**](/windows/win32/api/directml/ne-directml-dml_create_device_flags) when you call [**DMLCreateDevice**](/windows/win32/api/directml/nf-directml-dmlcreatedevice).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="835e5-114">Сначала необходимо включить уровень отладки Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="835e5-114">You must first enable the Direct3D 12 debug layer.</span></span> <span data-ttu-id="835e5-115">А *затем* включите уровень отладки директмл, вызвав **дмлкреатедевице**.</span><span class="sxs-lookup"><span data-stu-id="835e5-115">And *then* enable the DirectML debug layer by calling **DMLCreateDevice**.</span></span>

<span data-ttu-id="835e5-116">После включения слоя отладки Директмл все ошибки Директмл или недопустимые вызовы API приведут к выдаче отладочной информации в качестве выходных данных отладки.</span><span class="sxs-lookup"><span data-stu-id="835e5-116">Once you've enabled the DirectML debug layer, any DirectML errors or invalid API calls will cause debugging information to be emitted as debug output.</span></span> <span data-ttu-id="835e5-117">Пример приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="835e5-117">Here's an example.</span></span>

```console
DML_OPERATOR_CONVOLUTION: invalid D3D12_HEAP_TYPE. DirectML requires all bound buffers to be D3D12_HEAP_TYPE_DEFAULT.
```

## <a name="see-also"></a><span data-ttu-id="835e5-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="835e5-118">See also</span></span>

* [<span data-ttu-id="835e5-119">Функция Дмлкреатедевице</span><span class="sxs-lookup"><span data-stu-id="835e5-119">DMLCreateDevice function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice)
* [<span data-ttu-id="835e5-120">Доступные функции — по запросу</span><span class="sxs-lookup"><span data-stu-id="835e5-120">Available Features-on-Demand</span></span>](/windows-hardware/manufacture/desktop/features-on-demand-non-language-fod)
* [<span data-ttu-id="835e5-121">Использование проверки на основе GPU с уровнем отладки Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="835e5-121">Use GPU-based validation with the Direct3D 12 Debug Layer</span></span>](/windows/desktop/direct3d12/using-d3d12-debug-layer-gpu-based-validation)
* [<span data-ttu-id="835e5-122">Справочник по отладочному слою Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="835e5-122">Direct3D 12 Debug Layer reference</span></span>](/windows/desktop/direct3d12/direct3d-12-sdklayers-reference)
