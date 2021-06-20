---
title: Свойство Enabled (объект Аудиуутпут)
description: Сведения о включенном свойстве объекта Аудиуутпут. Microsoft Agent является устаревшим в Windows 7.
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b807b4cadcc9a0157b4efa400dd9d0e3cb5cf21a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407347"
---
# <a name="enabled-property-audiooutput-object"></a><span data-ttu-id="fcb06-104">Свойство Enabled (объект Аудиуутпут)</span><span class="sxs-lookup"><span data-stu-id="fcb06-104">Enabled Property (AudioOutput Object)</span></span>

<span data-ttu-id="fcb06-105">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fcb06-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="fcb06-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="fcb06-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="fcb06-107">Возвращает логическое значение, указывающее, включены ли выходные данные звука (речь).</span><span class="sxs-lookup"><span data-stu-id="fcb06-107">Returns a Boolean indicating whether audio (spoken) output is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="fcb06-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="fcb06-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="fcb06-109">*агент \* \* *. Аудиуутпут. Enabled**</span><span class="sxs-lookup"><span data-stu-id="fcb06-109">*agent\*\*\*.AudioOutput.Enabled*\*</span></span>



| <span data-ttu-id="fcb06-110">Значение</span><span class="sxs-lookup"><span data-stu-id="fcb06-110">Value</span></span>     | <span data-ttu-id="fcb06-111">Описание</span><span class="sxs-lookup"><span data-stu-id="fcb06-111">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="fcb06-112">**True**</span><span class="sxs-lookup"><span data-stu-id="fcb06-112">**True**</span></span>  | <span data-ttu-id="fcb06-113">Параметры Включен речевой вывод.</span><span class="sxs-lookup"><span data-stu-id="fcb06-113">(Default) Spoken audio output is enabled.</span></span> |
| <span data-ttu-id="fcb06-114">**False**</span><span class="sxs-lookup"><span data-stu-id="fcb06-114">**False**</span></span> | <span data-ttu-id="fcb06-115">Речевое Выходное звуковое сопровождение отключено.</span><span class="sxs-lookup"><span data-stu-id="fcb06-115">Spoken audio output is disabled.</span></span>          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fcb06-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="fcb06-116">Remarks</span></span>

<span data-ttu-id="fcb06-117">Это свойство отражает параметр воспроизведение аудио вывода на странице вывод страницы свойств агента (дополнительные параметры символов).</span><span class="sxs-lookup"><span data-stu-id="fcb06-117">This property reflects the Play Audio Output option on the Output page of the Agent property sheet (Advanced Character Options).</span></span> <span data-ttu-id="fcb06-118">Если свойство [**Enabled**](enabled-property.md) возвращает **значение true**, то метод [**говорите**](speak-method.md) создает выходные данные, если установлен совместимый обработчик TTS, или для речевого вывода используются звуковые файлы.</span><span class="sxs-lookup"><span data-stu-id="fcb06-118">When the [**Enabled**](enabled-property.md) property returns **True**, the [**Speak**](speak-method.md) method produces audio output if a compatible TTS engine is installed or you use sound files for spoken output.</span></span> <span data-ttu-id="fcb06-119">При возврате значения **false** это означает, что речевой вывод не установлен или отключен пользователем.</span><span class="sxs-lookup"><span data-stu-id="fcb06-119">When it returns **False**, it means that speech output is not installed or has been disabled by the user.</span></span> <span data-ttu-id="fcb06-120">Параметр свойства применяется ко всем символам агента и доступен только для чтения; только пользователь может установить это значение свойства.</span><span class="sxs-lookup"><span data-stu-id="fcb06-120">The property setting applies to all Agent characters and is read-only; only the user can set this property value.</span></span>

## <a name="see-also"></a><span data-ttu-id="fcb06-121">См. также</span><span class="sxs-lookup"><span data-stu-id="fcb06-121">See Also</span></span>

[<span data-ttu-id="fcb06-122">Событие Ажентпропертичанже</span><span class="sxs-lookup"><span data-stu-id="fcb06-122">AgentPropertyChange Event</span></span>](agentpropertychange-event.md)


 

 




