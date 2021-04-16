---
title: Ускорение с помощью GPU в WSL
description: Direct Машинное обучение (Директмл) — Микрографический процессор — акцеллератион в подсистеме Windows для Linux
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: 217a1763c0030a856e10a822cbd9f2642480c056
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105719152"
---
# <a name="gpu-accelerated-ml-training"></a><span data-ttu-id="a7f8b-103">Быстрое обучение GPU с ускорением МАШИНного обучения</span><span class="sxs-lookup"><span data-stu-id="a7f8b-103">GPU accelerated ML training</span></span>

![Графическое изображение Windows ML](images/winml-graphic.png)

<span data-ttu-id="a7f8b-105">В этой документации описывается, что сейчас поддерживается предварительным обучением GPU (машинного обучения) для [подсистемы Windows для Linux](/windows/wsl/about) (WSL) и собственных Windows.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-105">This documentation covers what is currently supported by the GPU accelerated machine learning (ML) training preview for the [Windows Subsystem for Linux](/windows/wsl/about) (WSL) and native Windows.</span></span>  

<span data-ttu-id="a7f8b-106">Эта предварительная версия поддерживает как профессиональные, так и начинающие сценарии.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-106">This preview supports both professional and beginner scenarios.</span></span> <span data-ttu-id="a7f8b-107">Ниже приведены указатели на пошаговые инструкции по настройке системы в зависимости от уровня опыта в ML, поставщика GPU и библиотеки программного обеспечения, которую вы собираетесь использовать.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-107">Below you will find pointers to step-by-step guides on how to get your system setup depending on your level of expertise in ML, GPU vendor, and the software library you intend to use.</span></span> 

> [!NOTE]
> <span data-ttu-id="a7f8b-108">Следующие функции доступны в предварительной версии и могут изменяться.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-108">The following features are in preview, and are subject to change.</span></span>


## <a name="professionals"></a><span data-ttu-id="a7f8b-109">ИТ специалистов</span><span class="sxs-lookup"><span data-stu-id="a7f8b-109">Professionals</span></span>

<span data-ttu-id="a7f8b-110">Если вы являетесь профессиональным анализу данных, использующих собственную среду Linux в повседневной среде для разработки и экспериментирования во внутреннем цикле, а у вас есть графический процессор NVIDIA, рекомендуется настроить [предварительную версию NVIDIA CUDA в WSL 2.](gpu-cuda-in-wsl.md)</span><span class="sxs-lookup"><span data-stu-id="a7f8b-110">If you’re a professional data scientist that uses a native Linux environment day-to-day for inner-loop ML development and experimentation, and you have an NVIDIA GPU, we recommend setting up the [NVIDIA CUDA preview in WSL 2.](gpu-cuda-in-wsl.md)</span></span>

## <a name="students-and-beginners"></a><span data-ttu-id="a7f8b-111">Студенты и начинающие</span><span class="sxs-lookup"><span data-stu-id="a7f8b-111">Students and beginners</span></span> 

<span data-ttu-id="a7f8b-112">Если вы являетесь студентом или начинаем начать создавать знания в пространстве машинного обучения, рекомендуем настроить TensorFlow с помощью серверного пакета Директмл.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-112">If you’re a student or beginner looking to start building your knowledge in the ML space, we recommend setting up the TensorFlow with DirectML backend package.</span></span> <span data-ttu-id="a7f8b-113">В настоящее время этот пакет ускоряет рабочие процессы на процессорах AMD и Intel GPU.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-113">This package currently accelerates workflows on AMD and Intel GPUs.</span></span> <span data-ttu-id="a7f8b-114">В ближайшее время ожидается поддержка видеопроцессоров NVIDIA.</span><span class="sxs-lookup"><span data-stu-id="a7f8b-114">Support for NVIDIA GPUs is coming soon.</span></span> 

<span data-ttu-id="a7f8b-115">Для тех, кто больше знаком с собственной средой Linux, Приступая к работе с рабочими процессами машинного обучения, мы рекомендуем запускать [TensorFlow с пакетом директмл внутри WSL 2](gpu-tensorflow-wsl.md).</span><span class="sxs-lookup"><span data-stu-id="a7f8b-115">For those more familiar with a native Linux environment that are getting started with ML workflows, we recommend running the [TensorFlow with DirectML package inside WSL 2](gpu-tensorflow-wsl.md).</span></span> 

<span data-ttu-id="a7f8b-116">Для тех, кто знаком с Windows, Приступая к работе с рабочими процессами машинного обучения, рекомендуется настроить [TensorFlow с пакетом директмл в собственных окнах](gpu-tensorflow-windows.md).</span><span class="sxs-lookup"><span data-stu-id="a7f8b-116">For those more familiar with Windows that are getting started with ML workflows, we recommend setting up the [TensorFlow with DirectML package on native Windows](gpu-tensorflow-windows.md).</span></span> 

## <a name="next-steps"></a><span data-ttu-id="a7f8b-117">Дальнейшие шаги</span><span class="sxs-lookup"><span data-stu-id="a7f8b-117">Next steps</span></span>

* <span data-ttu-id="a7f8b-118">[Включите предварительную версию NVIDIA CUDA в WSL 2](gpu-cuda-in-wsl.md).</span><span class="sxs-lookup"><span data-stu-id="a7f8b-118">[Enable NVIDIA CUDA preview in WSL 2](gpu-cuda-in-wsl.md).</span></span>
* <span data-ttu-id="a7f8b-119">[Включить TensorFlow с пакетом директмл внутри WSL 2](gpu-tensorflow-wsl.md).</span><span class="sxs-lookup"><span data-stu-id="a7f8b-119">[Enable TensorFlow with DirectML package inside WSL 2](gpu-tensorflow-wsl.md).</span></span>
* <span data-ttu-id="a7f8b-120">[Включите TensorFlow с пакетом директмл в собственных окнах](gpu-tensorflow-windows.md).</span><span class="sxs-lookup"><span data-stu-id="a7f8b-120">[Enable TensorFlow with DirectML package on native Windows](gpu-tensorflow-windows.md).</span></span>