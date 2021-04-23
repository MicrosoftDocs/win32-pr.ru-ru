---
description: В подразделах этого раздела приведены справочные спецификации для структурного стека входных данных устройства указателя.
ms.assetid: 33DCB172-8D95-4205-AE2E-ADD7F3BF988A
title: Структуры (входные данные устройства-указателя)
ms.topic: article
ms.date: 02/05/2020
ms.openlocfilehash: 988a66a65581cf97406ace5481f115b15a29329a
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/26/2021
ms.locfileid: "105721081"
---
# <a name="pointer-device-input-stack-structures"></a><span data-ttu-id="971c7-103">Структуры стека входных данных устройства указателя</span><span class="sxs-lookup"><span data-stu-id="971c7-103">Pointer Device Input Stack structures</span></span>

<span data-ttu-id="971c7-104">В подразделах этого раздела приведены справочные спецификации для структурного [стека входных данных устройства указателя](pointer-device-stack-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="971c7-104">The topics in this section provide the reference specifications for [Pointer Device Input Stack](pointer-device-stack-portal.md) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="971c7-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="971c7-105">In this section</span></span>

| <span data-ttu-id="971c7-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="971c7-106">Topic</span></span> | <span data-ttu-id="971c7-107">Описание</span><span class="sxs-lookup"><span data-stu-id="971c7-107">Description</span></span> |
|---|---|
| [<span data-ttu-id="971c7-108">**POINTER_DEVICE_CURSOR_INFO**</span><span class="sxs-lookup"><span data-stu-id="971c7-108">**POINTER_DEVICE_CURSOR_INFO**</span></span>](/windows/win32/api/winuser/ns-winuser-pointer_device_cursor_info)<br/> | <span data-ttu-id="971c7-109">Содержит сопоставления ИДЕНТИФИКАТОРов курсоров для устройств указателей.</span><span class="sxs-lookup"><span data-stu-id="971c7-109">Contains cursor ID mappings for pointer devices.</span></span><br/> |
| [<span data-ttu-id="971c7-110">**POINTER_DEVICE_INFO**</span><span class="sxs-lookup"><span data-stu-id="971c7-110">**POINTER_DEVICE_INFO**</span></span>](/windows/win32/api/winuser/ns-winuser-pointer_device_info)<br/> | <span data-ttu-id="971c7-111">Содержит сведения об устройстве-указателе.</span><span class="sxs-lookup"><span data-stu-id="971c7-111">Contains information about a pointer device.</span></span> <span data-ttu-id="971c7-112">Массив этих структур возвращается из функции [**жетпоинтердевицес**](/windows/win32/api/winuser/nf-winuser-getpointerdevices) .</span><span class="sxs-lookup"><span data-stu-id="971c7-112">An array of these structures is returned from the [**GetPointerDevices**](/windows/win32/api/winuser/nf-winuser-getpointerdevices) function.</span></span> <span data-ttu-id="971c7-113">При вызове функции [**жетпоинтердевице**](/windows/win32/api/winuser/nf-winuser-getpointerdevice) возвращается одна структура.</span><span class="sxs-lookup"><span data-stu-id="971c7-113">A single structure is returned from a call to the [**GetPointerDevice**](/windows/win32/api/winuser/nf-winuser-getpointerdevice) function.</span></span> <br/> |
| [<span data-ttu-id="971c7-114">**POINTER_DEVICE_PROPERTY**</span><span class="sxs-lookup"><span data-stu-id="971c7-114">**POINTER_DEVICE_PROPERTY**</span></span>](/windows/win32/api/winuser/ns-winuser-pointer_device_property)<br/> | <span data-ttu-id="971c7-115">Содержит свойства устройства (устройство HID (HID) глобальные элементы, соответствующие использованию HID.</span><span class="sxs-lookup"><span data-stu-id="971c7-115">Contains device properties (Human Interface Device (HID) global items that correspond to HID usages).</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="971c7-116">См. также</span><span class="sxs-lookup"><span data-stu-id="971c7-116">Related topics</span></span>

[<span data-ttu-id="971c7-117">Указатель на входной стек устройства указателя</span><span class="sxs-lookup"><span data-stu-id="971c7-117">Pointer Device Input Stack Reference</span></span>](unified-input-stack-reference.md)
