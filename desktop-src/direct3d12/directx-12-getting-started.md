---
title: Основные сведения о Direct3D 12
description: Чтобы написать трехмерные игры и приложения для Windows 10 и Windows 10 Mobile, необходимо ознакомиться с основами технологии Direct3D 12 и как подготовиться к использованию в играх и приложениях.
ms.assetid: DED7A434-FCD4-4F41-8B2C-E5AE6E48430F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1353c8c66fd401e364b9db302463f164f757c9ac
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549037"
---
# <a name="understanding-direct3d-12"></a><span data-ttu-id="75dae-103">Основные сведения о Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="75dae-103">Understanding Direct3D 12</span></span>

<span data-ttu-id="75dae-104">Чтобы написать трехмерные игры и приложения для Windows 10 и Windows 10 Mobile, необходимо ознакомиться с основами технологии Direct3D 12 и как подготовиться к использованию в играх и приложениях.</span><span class="sxs-lookup"><span data-stu-id="75dae-104">To write 3D games and apps for Windows 10 and Windows 10 Mobile, you must understand the basics of the Direct3D 12 technology, and how to prepare to use it in your games and apps.</span></span>

<span data-ttu-id="75dae-105">Используйте подразделы этого раздела для настройки и изучения среды, в которой будут программироваться приложения и игры с помощью Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="75dae-105">Use the topics in this section to set up and learn about the environment in which you will program your apps and games with Direct3D 12.</span></span> <span data-ttu-id="75dae-106">Это содержимое также поможет перенести приложения Direct3D 11 и игры на Direct3D 12, чтобы воспользоваться преимуществами функций и эффективности Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="75dae-106">This content will also help you to port your Direct3D 11 apps and games to Direct3D 12, so you can take advantage of Direct3D 12 features and efficiencies.</span></span>

<span data-ttu-id="75dae-107">Для программирования с помощью Direct3D 12 необходимы следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="75dae-107">To program with Direct3D 12, you need these components:</span></span>

-   <span data-ttu-id="75dae-108">Аппаратная платформа с графическим процессором, совместимым с Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="75dae-108">A hardware platform with a Direct3D 12-compatible GPU</span></span>
-   <span data-ttu-id="75dae-109">[Отображение драйверов](/previous-versions//ff569172(v=vs.85)) , поддерживающих модель Windows дисплея (WDDM) 2,0</span><span class="sxs-lookup"><span data-stu-id="75dae-109">[Display drivers](/previous-versions//ff569172(v=vs.85)) that support the Windows Display Driver Model (WDDM) 2.0</span></span>

## <a name="in-this-section"></a><span data-ttu-id="75dae-110">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="75dae-110">In this section</span></span>



| <span data-ttu-id="75dae-111">Раздел</span><span class="sxs-lookup"><span data-stu-id="75dae-111">Topic</span></span>                                                                                                               | <span data-ttu-id="75dae-112">Описание</span><span class="sxs-lookup"><span data-stu-id="75dae-112">Description</span></span>                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75dae-113">Установка среды программирования Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="75dae-113">Direct3D 12 Programming Environment Setup</span></span>](directx-12-programming-environment-set-up.md)<br/>               | <span data-ttu-id="75dae-114">Описывает установку, средства и поддерживаемые библиотеки, которые составляют эффективную среду разработки Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="75dae-114">Describes the installation, tools and supported libraries that make up a productive Direct3D 12 development environment.</span></span> <br/>                              |
| [<span data-ttu-id="75dae-115">Создание базового компонента Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="75dae-115">Creating a Basic Direct3D 12 Component</span></span>](creating-a-basic-direct3d-12-component.md)<br/>                     | <span data-ttu-id="75dae-116">В этом разделе описывается поток вызова для создания базового компонента Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="75dae-116">This topic describes the call flow to create a basic Direct3D 12 component.</span></span><br/>                                                                            |
| [<span data-ttu-id="75dae-117">Важные изменения с Direct3D 11 до Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="75dae-117">Important Changes from Direct3D 11 to Direct3D 12</span></span>](important-changes-from-directx-11-to-directx-12.md)<br/> | <span data-ttu-id="75dae-118">Direct3D 12 представляет значительный уход с модели программирования Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="75dae-118">Direct3D 12 represents a significant departure from the Direct3D 11 programming model.</span></span> <span data-ttu-id="75dae-119">Direct3D 12 позволяет приложениям ближе к оборудованию, чем когда-либо ранее.</span><span class="sxs-lookup"><span data-stu-id="75dae-119">Direct3D 12 lets apps get closer to hardware than ever before.</span></span> <br/> |
| [<span data-ttu-id="75dae-120">Уровни компонентов оборудования</span><span class="sxs-lookup"><span data-stu-id="75dae-120">Hardware Feature Levels</span></span>](hardware-feature-levels.md)<br/>                                                   | <span data-ttu-id="75dae-121">Описание функциональных возможностей уровней "11 \_ 0 – 12 \_ 1" для аппаратных компонентов.</span><span class="sxs-lookup"><span data-stu-id="75dae-121">Describes the functionality of the 11\_0 through 12\_1 hardware feature levels.</span></span><br/>                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="75dae-122">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="75dae-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75dae-123">Руководство по программированию для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="75dae-123">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> </dl>

 

