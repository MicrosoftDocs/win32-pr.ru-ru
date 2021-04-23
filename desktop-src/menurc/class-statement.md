---
title: Оператор класса
description: Определяет класс диалогового окна.
ms.assetid: 7c4325fe-66a4-4bb2-9c99-04b3ff590e7a
keywords:
- Меню инструкций класса и другие ресурсы
topic_type:
- apiref
api_name:
- CLASS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d31eba66a1e4527a24a55a24e4623f3c49dc204
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987443"
---
# <a name="class-statement"></a><span data-ttu-id="d7a61-104">Оператор класса</span><span class="sxs-lookup"><span data-stu-id="d7a61-104">CLASS statement</span></span>

<span data-ttu-id="d7a61-105">Определяет класс диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="d7a61-105">Defines the class of the dialog box.</span></span>

<span data-ttu-id="d7a61-106">Оператор **Class** появляется в необязательном разделе перед параметром main инструкции [**диалогового окна**](dialog-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="d7a61-106">The **CLASS** statement appears in the optional section before a [**DIALOG**](dialog-resource.md) statement's main.</span></span> <span data-ttu-id="d7a61-107">Если класс не задан, используется стандартный класс диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="d7a61-107">If no class is given, the standard dialog class is used.</span></span>

``` syntax
CLASS class
```

<dl> <dt>

<span data-ttu-id="d7a61-108"><span id="class"></span><span id="CLASS"></span>*см*</span><span class="sxs-lookup"><span data-stu-id="d7a61-108"><span id="class"></span><span id="CLASS"></span>*class*</span></span>
</dt> <dd>

<span data-ttu-id="d7a61-109">16-разрядное целое число без знака или строка, заключенная в двойные кавычки ("), которая определяет класс диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="d7a61-109">A 16-bit unsigned integer or a string, enclosed in double quotation marks ("), that identifies the class of the dialog box.</span></span> <span data-ttu-id="d7a61-110">Если процедура окна для класса не обрабатывает сообщение, отправленное в него, необходимо вызвать функцию [**дефдлгпрок**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) , чтобы убедиться, что все сообщения правильно обрабатывались для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="d7a61-110">If the window procedure for the class does not process a message sent to it, it must call the [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) function to ensure that all messages are handled properly for the dialog box.</span></span> <span data-ttu-id="d7a61-111">Закрытый класс может использовать **дефдлгпрок** в качестве процедуры окна по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d7a61-111">A private class can use **DefDlgProc** as the default window procedure.</span></span> <span data-ttu-id="d7a61-112">Класс должен быть зарегистрирован с элементом **кбвндекстра** структуры [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) , равным **длгвиндовекстра**.</span><span class="sxs-lookup"><span data-stu-id="d7a61-112">The class must be registered with the **cbWndExtra** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure set to **DLGWINDOWEXTRA**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7a61-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7a61-113">Remarks</span></span>

<span data-ttu-id="d7a61-114">Оператор **Class** следует использовать только с особыми случаями, поскольку он переопределяет нормальную обработку диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="d7a61-114">The **CLASS** statement should only be used with special cases, because it overrides the normal processing of a dialog box.</span></span> <span data-ttu-id="d7a61-115">Оператор **класса** преобразует диалоговое окно в окно указанного класса; в зависимости от класса это может привести к нежелательным результатам.</span><span class="sxs-lookup"><span data-stu-id="d7a61-115">The **CLASS** statement converts a dialog box to a window of the specified class; depending on the class, this could give undesirable results.</span></span> <span data-ttu-id="d7a61-116">Не используйте переопределенные имена классов элементов управления с этой инструкцией.</span><span class="sxs-lookup"><span data-stu-id="d7a61-116">Do not use the redefined control-class names with this statement.</span></span>

## <a name="examples"></a><span data-ttu-id="d7a61-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="d7a61-117">Examples</span></span>

<span data-ttu-id="d7a61-118">В следующем примере демонстрируется использование оператора **Class** :</span><span class="sxs-lookup"><span data-stu-id="d7a61-118">The following example demonstrates the use of the **CLASS** statement:</span></span>

``` syntax
CLASS "myclass" 
```

## <a name="see-also"></a><span data-ttu-id="d7a61-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7a61-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7a61-120">**дефдлгпрок**</span><span class="sxs-lookup"><span data-stu-id="d7a61-120">**DefDlgProc**</span></span>](/windows/win32/api/winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[<span data-ttu-id="d7a61-121">**Откроется**</span><span class="sxs-lookup"><span data-stu-id="d7a61-121">**DIALOG**</span></span>](dialog-resource.md)
</dt> </dl>

 

 