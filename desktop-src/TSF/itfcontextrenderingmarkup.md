---
title: Интерфейс Итфконтекстрендерингмаркуп
description: Интерфейс Итфконтекстрендерингмаркуп реализуется диспетчером TSF и используется приложениями. Этот интерфейс можно получить с помощью Икуеринтерфаце из объекта ITfContext. Этот интерфейс помогает приложению перечислять данные отрисовки.
ms.assetid: 733d2db2-f9e9-4b78-af13-adc03825bf2b
keywords:
- Платформа текстовых служб интерфейса Итфконтекстрендерингмаркуп
- Платформа текстовых служб интерфейса Итфконтекстрендерингмаркуп, описание
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b71e977665a4b3a6e817ef782ee558064e0986a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890817"
---
# <a name="itfcontextrenderingmarkup-interface"></a><span data-ttu-id="f4e9e-107">Интерфейс Итфконтекстрендерингмаркуп</span><span class="sxs-lookup"><span data-stu-id="f4e9e-107">ITfContextRenderingMarkup interface</span></span>

<span data-ttu-id="f4e9e-108">Интерфейс **итфконтекстрендерингмаркуп** реализуется диспетчером TSF и используется приложениями.</span><span class="sxs-lookup"><span data-stu-id="f4e9e-108">The **ITfContextRenderingMarkup** interface is implemented by TSF manager and used by applications.</span></span> <span data-ttu-id="f4e9e-109">Этот интерфейс можно получить с помощью Икуеринтерфаце из объекта [ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext) .</span><span class="sxs-lookup"><span data-stu-id="f4e9e-109">This interface can be retrieved using IQueryInterface from [ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext) object.</span></span> <span data-ttu-id="f4e9e-110">Этот интерфейс помогает приложению перечислять данные отрисовки.</span><span class="sxs-lookup"><span data-stu-id="f4e9e-110">This interface helps the application enumerate rendering information.</span></span>



| <span data-ttu-id="f4e9e-111">Методы Итфконтекстрендерингмаркуп</span><span class="sxs-lookup"><span data-stu-id="f4e9e-111">ITfContextRenderingMarkup methods</span></span>                                                | <span data-ttu-id="f4e9e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f4e9e-112">Description</span></span>                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="f4e9e-113">жетрендерингмаркуп</span><span class="sxs-lookup"><span data-stu-id="f4e9e-113">GetRenderingMarkup</span></span>](itfcontextrenderingmarkup-getrenderingmarkup.md)           | <span data-ttu-id="f4e9e-114">Извлекает перечислитель разметки отрисовки для заданного диапазона.</span><span class="sxs-lookup"><span data-stu-id="f4e9e-114">Retrieves an enumerator of the rendering markups for the given range.</span></span> |
| [<span data-ttu-id="f4e9e-115">финднекстрендерингмаркуп</span><span class="sxs-lookup"><span data-stu-id="f4e9e-115">FindNextRenderingMarkup</span></span>](itfcontextrenderingmarkup-findnextrenderingmarkup.md) | <span data-ttu-id="f4e9e-116">Эта функция не реализована.</span><span class="sxs-lookup"><span data-stu-id="f4e9e-116">This function is not implemented.</span></span> <span data-ttu-id="f4e9e-117">Он всегда возвращает E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="f4e9e-117">It always returns E\_NOTIMPL.</span></span>       |



 

## <a name="members"></a><span data-ttu-id="f4e9e-118">Элементы</span><span class="sxs-lookup"><span data-stu-id="f4e9e-118">Members</span></span>

<span data-ttu-id="f4e9e-119">Интерфейс **итфконтекстрендерингмаркуп** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="f4e9e-119">The **ITfContextRenderingMarkup** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4e9e-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f4e9e-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f4e9e-121">Этот интерфейс в настоящее время не находится в файлах общедоступного заголовка.</span><span class="sxs-lookup"><span data-stu-id="f4e9e-121">This interface is not currently in the public header files.</span></span> <span data-ttu-id="f4e9e-122">Чтобы использовать этот API, необходимо скомпилировать [прототип](prototypes.md)с помощью MIDL.</span><span class="sxs-lookup"><span data-stu-id="f4e9e-122">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

 