---
title: Интерфейс Иенумтфрендерингмаркуп
description: Интерфейс Иенумтфрендерингмаркуп реализуется диспетчером TSF и используется приложениями. Этот интерфейс можно извлечь с помощью Итфконтекстрендерингмаркуп Жетрендерингмаркуп и перечислить сведения о разметке визуализации.
ms.assetid: 6062a6f5-f973-4cd5-94d3-05aa418e0198
keywords:
- Платформа текстовых служб интерфейса Иенумтфрендерингмаркуп
- Платформа текстовых служб интерфейса Иенумтфрендерингмаркуп, описание
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3005c8fe37a26b11f5155b639f8c151cf59c2cf0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070415"
---
# <a name="ienumtfrenderingmarkup-interface"></a><span data-ttu-id="7edf2-106">Интерфейс Иенумтфрендерингмаркуп</span><span class="sxs-lookup"><span data-stu-id="7edf2-106">IEnumTfRenderingMarkup interface</span></span>

<span data-ttu-id="7edf2-107">Интерфейс **иенумтфрендерингмаркуп** реализуется диспетчером TSF и используется приложениями.</span><span class="sxs-lookup"><span data-stu-id="7edf2-107">The **IEnumTfRenderingMarkup** interface is implemented by TSF Manager and used by applications.</span></span> <span data-ttu-id="7edf2-108">Этот интерфейс может быть извлечен с помощью [итфконтекстрендерингмаркуп:: жетрендерингмаркуп](itfcontextrenderingmarkup-getrenderingmarkup.md) и перечисляет сведения о разметке отрисовки.</span><span class="sxs-lookup"><span data-stu-id="7edf2-108">This interface can be retrieved by [ITfContextRenderingMarkup::GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md) and enumerates the rendering markup information.</span></span>



| <span data-ttu-id="7edf2-109">Методы Иенумтфрендерингмаркуп</span><span class="sxs-lookup"><span data-stu-id="7edf2-109">IEnumTfRenderingMarkup methods</span></span>            | <span data-ttu-id="7edf2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="7edf2-110">Description</span></span>                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7edf2-111">Клонировать</span><span class="sxs-lookup"><span data-stu-id="7edf2-111">Clone</span></span>](ienumtfrenderingmarkup-clone.md) | <span data-ttu-id="7edf2-112">Метод **иенумтфрендерингмаркуп:: Clone** создает копию объекта перечислителя.</span><span class="sxs-lookup"><span data-stu-id="7edf2-112">The **IEnumTfRenderingMarkup::Clone** method creates a copy of the enumerator object.</span></span>                                                                  |
| [<span data-ttu-id="7edf2-113">Вперед</span><span class="sxs-lookup"><span data-stu-id="7edf2-113">Next</span></span>](ienumtfrenderingmarkup-next.md)   | <span data-ttu-id="7edf2-114">Метод **иенумтфрендерингмаркуп:: Next** получает от текущей позицией указанное число элементов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="7edf2-114">The **IEnumTfRenderingMarkup::Next** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>          |
| [<span data-ttu-id="7edf2-115">Сброс</span><span class="sxs-lookup"><span data-stu-id="7edf2-115">Reset</span></span>](ienumtfrenderingmarkup-reset.md) | <span data-ttu-id="7edf2-116">Метод **иенумтфрендерингмаркуп:: Reset** сбрасывает объект перечислителя, перемещая текущую точку в начало последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="7edf2-116">The **IEnumTfRenderingMarkup::Reset** method resets the enumerator object by moving the current position to the beginning of the enumeration sequence.</span></span> |
| [<span data-ttu-id="7edf2-117">Skip</span><span class="sxs-lookup"><span data-stu-id="7edf2-117">Skip</span></span>](ienumtfrenderingmarkup-skip.md)   | <span data-ttu-id="7edf2-118">Метод **иенумтфрендерингмаркуп:: Skip** получает от текущей позицией указанное число элементов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="7edf2-118">The **IEnumTfRenderingMarkup::Skip** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>          |



 

## <a name="members"></a><span data-ttu-id="7edf2-119">Элементы</span><span class="sxs-lookup"><span data-stu-id="7edf2-119">Members</span></span>

<span data-ttu-id="7edf2-120">Интерфейс **иенумтфрендерингмаркуп** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="7edf2-120">The **IEnumTfRenderingMarkup** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="remarks"></a><span data-ttu-id="7edf2-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7edf2-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7edf2-122">Этот интерфейс в настоящее время не находится в файлах общедоступного заголовка.</span><span class="sxs-lookup"><span data-stu-id="7edf2-122">This interface is not currently in the public header files.</span></span> <span data-ttu-id="7edf2-123">Чтобы использовать этот API, необходимо скомпилировать [прототип](prototypes.md)с помощью MIDL.</span><span class="sxs-lookup"><span data-stu-id="7edf2-123">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

 