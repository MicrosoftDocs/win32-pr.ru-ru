---
description: Отладочная версия подсистемы XAudio2 проверяет параметры и предоставляет подробные сообщения о предупреждениях и ошибках.
ms.assetid: a7aaebf9-98d4-e96c-993d-b0d0b7074788
title: Средства отладки XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc50e710f30969e024078eeaf2660545e1da45c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810457"
---
# <a name="xaudio2-debugging-facilities"></a><span data-ttu-id="6ad8b-103">Средства отладки XAudio2</span><span class="sxs-lookup"><span data-stu-id="6ad8b-103">XAudio2 Debugging Facilities</span></span>

<span data-ttu-id="6ad8b-104">Отладочная версия подсистемы XAudio2 проверяет параметры и предоставляет подробные сообщения о предупреждениях и ошибках.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-104">The debug version of the XAudio2 engine validates parameters, and provides detailed warning and error messages.</span></span>

## <a name="setting-the-debug-logging-level-at-run-time"></a><span data-ttu-id="6ad8b-105">Настройка уровня ведения журнала отладки во время выполнения</span><span class="sxs-lookup"><span data-stu-id="6ad8b-105">Setting the Debug Logging Level at Run Time</span></span>

<span data-ttu-id="6ad8b-106">Уровень отладочной информации, отображаемой XAudio2, можно задать в любое время, заполнив структуру [**\_ \_ конфигурации отладки XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration) с флагами для требуемого уровня ведения журнала, а затем передать структуру методу [**IXAudio2:: сетдебугконфигуратион**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration) .</span><span class="sxs-lookup"><span data-stu-id="6ad8b-106">You can set the level of debugging information shown by XAudio2 at any time by filling out an [**XAUDIO2\_DEBUG\_CONFIGURATION**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration) structure with the flags for the desired logging level, and then pass the structure to the [**IXAudio2::SetDebugConfiguration**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration) method.</span></span> <span data-ttu-id="6ad8b-107">Значения, передаваемые методу **IXAudio2:: сетдебугконфигуратион** , всегда переопределяют все значения по умолчанию, заданные в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-107">Values passed to the **IXAudio2::SetDebugConfiguration** method always override any default values that were set in the Windows registry.</span></span>

## <a name="debug-support"></a><span data-ttu-id="6ad8b-108">Поддержка отладки</span><span class="sxs-lookup"><span data-stu-id="6ad8b-108">Debug Support</span></span>

<span data-ttu-id="6ad8b-109">Средства отладки всегда доступны для XAUDIO2 в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-109">The debugging facilities are always available for XAUDIO2 in Windows 8.</span></span>

<span data-ttu-id="6ad8b-110">В версиях XAUDIO2 для DirectX SDK необходимо использовать **\_ \_ модуль отладки XAUDIO2** при создании объекта XAUDIO2 с [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) , а для поддержки отладки в системе должна быть установлена среда выполнения разработчика DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="6ad8b-110">For the DirectX SDK versions of XAUDIO2, you must use **XAUDIO2\_DEBUG\_ENGINE** when creating the XAUDIO2 object with [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) and the system must have the DirectX SDK Developer Runtime installed for debugging to be supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ad8b-111">См. также</span><span class="sxs-lookup"><span data-stu-id="6ad8b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ad8b-112">Отладочные средства</span><span class="sxs-lookup"><span data-stu-id="6ad8b-112">Debugging Facilities</span></span>](debugging-facilities.md)
</dt> <dt>

[<span data-ttu-id="6ad8b-113">Справочник по программированию в XAudio2</span><span class="sxs-lookup"><span data-stu-id="6ad8b-113">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 
