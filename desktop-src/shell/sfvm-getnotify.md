---
description: Уведомление, отправленное в объект обратного вызова представления для указания расположений и событий, которые должны быть зарегистрированы для событий уведомления об изменении.
title: Сообщение SFVM_GETNOTIFY (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 87933217-dfa9-4aaf-9630-fa2c302b18fa
api_name:
- SFVM_GETNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f766ee74463dd820c0b55d501d5002a3378a97b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265311"
---
# <a name="sfvm_getnotify-message"></a><span data-ttu-id="07262-103">\_Сообщение сфвм</span><span class="sxs-lookup"><span data-stu-id="07262-103">SFVM\_GETNOTIFY message</span></span>

<span data-ttu-id="07262-104">Уведомление, отправленное в объект обратного вызова представления для указания расположений и событий, которые должны быть зарегистрированы для событий уведомления об изменении.</span><span class="sxs-lookup"><span data-stu-id="07262-104">Notification sent to the view callback object to specify the locations and events that should be registered for change notification events.</span></span> <span data-ttu-id="07262-105">После того как они зарегистрированы, при возникновении изменений в этих местах или событиях уведомляется объект обратного вызова представления.</span><span class="sxs-lookup"><span data-stu-id="07262-105">Once they are registered, when a change occurs in on of these locations or events, the view callback object is notified.</span></span> <span data-ttu-id="07262-106">Эти события отправляются в обратный вызов представления через [**сфвм \_ фснотифи**](sfvm-fsnotify.md) и затем обрабатываются представлением.</span><span class="sxs-lookup"><span data-stu-id="07262-106">These events are sent to the view callback through [**SFVM\_FSNOTIFY**](sfvm-fsnotify.md) and are then handled by the view.</span></span>


```C++
SFVM_GETNOTIFY 

    wParam = (WPARAM)(LPITEMIDLIST*) pidl;

    lParam = (LPARAM)(LONG*) lEvents;

            
```



## <a name="parameters"></a><span data-ttu-id="07262-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="07262-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07262-108">*Пидл* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="07262-108">*pidl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07262-109">Указатель на абсолютное IDList элемента, для которого должно быть зарегистрировано представление, чтобы получать уведомления об изменениях.</span><span class="sxs-lookup"><span data-stu-id="07262-109">A pointer to an absolute IDList of an item for which the view should register to be notified of changes.</span></span> <span data-ttu-id="07262-110">Как правило, это то же самое, что IDList в просматриваемом расположении, но может быть другим расположением.</span><span class="sxs-lookup"><span data-stu-id="07262-110">Typically, this is the same as the IDList of the location being viewed, but it can be another location.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="07262-111">Время существования этого значения принадлежит объекту обратного вызова представления.</span><span class="sxs-lookup"><span data-stu-id="07262-111">The lifetime of this value is owned by the view callback object.</span></span> <span data-ttu-id="07262-112">Объект обратного вызова представления является обязанностью создания, а затем освобождает это значение, когда оно больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="07262-112">It is the responsibility of the view callback object to create and then free this value when it is no longer needed.</span></span> <span data-ttu-id="07262-113">Для этого необходимо, чтобы объект обратного вызова View сохранял это значение.</span><span class="sxs-lookup"><span data-stu-id="07262-113">This requires that the view callback object stores this value.</span></span> <span data-ttu-id="07262-114">Как правило, значение может храниться в элементе **\_ пидлмонитор** объекта обратного вызова представления.</span><span class="sxs-lookup"><span data-stu-id="07262-114">Usually, the value can be stored in the **\_pidlMonitor** member of the view callback object.</span></span> <span data-ttu-id="07262-115">Правила владения для значения, возвращаемого через *Пидл* , являются нестандартными и нуждаются в особой осторожности.</span><span class="sxs-lookup"><span data-stu-id="07262-115">The ownership rules for the value returned through *pidl* are nonstandard and require special care.</span></span> <span data-ttu-id="07262-116">Объект обратного вызова представления должен владеть этим значением и гарантировать его освобождение до уничтожения самого объекта обратного вызова представления.</span><span class="sxs-lookup"><span data-stu-id="07262-116">The view callback object must own this value and ensure that it is not freed until the view callback object itself is destroyed.</span></span>

 

</dd> <dt>

<span data-ttu-id="07262-117">*левентс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="07262-117">*lEvents* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07262-118">Значение типа, содержащее одно или несколько значений ШКНЕ.</span><span class="sxs-lookup"><span data-stu-id="07262-118">A value that contains one or more SHCNE values.</span></span> <span data-ttu-id="07262-119">Список возможных значений см. в разделе [**шчанженотифи**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) .</span><span class="sxs-lookup"><span data-stu-id="07262-119">See [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) for a list of possible values.</span></span> <span data-ttu-id="07262-120">Объект обратного вызова View регистрируется для получения сообщения [**сфвм \_ фснотифи**](sfvm-fsnotify.md) при возникновении любого из связанных событий.</span><span class="sxs-lookup"><span data-stu-id="07262-120">The view callback object will register to receive an [**SFVM\_FSNOTIFY**](sfvm-fsnotify.md) message when any of the associated events occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07262-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07262-121">Return value</span></span>

<span data-ttu-id="07262-122">Пропускается, но должно возвращать S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="07262-122">Ignored, but should return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="07262-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="07262-123">Remarks</span></span>

<span data-ttu-id="07262-124">Если это сообщение обратного вызова не возвращает ненулевое значение для IDList или маски событий, представление не будет зарегистрировано для уведомлений об изменениях.</span><span class="sxs-lookup"><span data-stu-id="07262-124">If this callback message does not return a nonzero value for either the IDList or the events mask then the view will not register for change notifications.</span></span>

## <a name="examples"></a><span data-ttu-id="07262-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="07262-125">Examples</span></span>

<span data-ttu-id="07262-126">В следующем примере показан пример реализации кода обработчика представления функции обратного вызова для **сфвмного \_ уведомления**.</span><span class="sxs-lookup"><span data-stu-id="07262-126">The following sample shows an example implementation of the view callback function's handler code for **SFVM\_GETNOTIFY**.</span></span>


```C++
case SFVM_GETNOTIFY:
  *((LPITEMIDLIST*)wParam) = _pidl;    // Pass a reference whose lifetime this 
                                       // class is responsible for.
                                      
  *((LONG*)lParam) = SHCNE_DISKEVENTS; // A combination of all of the 
                                       // disk event identifiers.
                                       
   return S_OK;
```



## <a name="requirements"></a><span data-ttu-id="07262-127">Требования</span><span class="sxs-lookup"><span data-stu-id="07262-127">Requirements</span></span>



| <span data-ttu-id="07262-128">Требование</span><span class="sxs-lookup"><span data-stu-id="07262-128">Requirement</span></span> | <span data-ttu-id="07262-129">Значение</span><span class="sxs-lookup"><span data-stu-id="07262-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="07262-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07262-130">Minimum supported client</span></span><br/> | <span data-ttu-id="07262-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="07262-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="07262-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07262-132">Minimum supported server</span></span><br/> | <span data-ttu-id="07262-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="07262-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="07262-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="07262-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="07262-135"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="07262-135"><dt>Shlobj.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07262-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07262-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07262-137">**СФВМ \_ куерифснотифи**</span><span class="sxs-lookup"><span data-stu-id="07262-137">**SFVM\_QUERYFSNOTIFY**</span></span>](sfvm-queryfsnotify.md)
</dt> <dt>

[<span data-ttu-id="07262-138">**Ишеллфолдервиевкб:: Мессажесфвкб**</span><span class="sxs-lookup"><span data-stu-id="07262-138">**IShellFolderViewCB::MessageSFVCB**</span></span>](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)
</dt> </dl>

 

 
