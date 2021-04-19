---
description: Содержит атрибуты общего ресурса DDE, поддерживаемые диспетчером общих баз данных NetDDE (DSDM).
ms.assetid: f4101553-06ef-4f83-87c7-5b6fdf0467e5
title: Структура НДДЕШАРЕИНФО (Нддеапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDDESHAREINFO
api_type:
- HeaderDef
api_location:
- Nddeapi.h
ms.openlocfilehash: 975382272a4e2c7cc56b0ddf593905b4d745a48b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702923"
---
# <a name="nddeshareinfo-structure"></a><span data-ttu-id="aea55-103">Структура НДДЕШАРЕИНФО</span><span class="sxs-lookup"><span data-stu-id="aea55-103">NDDESHAREINFO structure</span></span>

<span data-ttu-id="aea55-104">\[Сетевой DDE больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="aea55-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="aea55-105">Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают НДДЕ \_ не \_ реализован.\]</span><span class="sxs-lookup"><span data-stu-id="aea55-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="aea55-106">Содержит атрибуты общего ресурса DDE, поддерживаемые диспетчером общих баз данных NetDDE (DSDM).</span><span class="sxs-lookup"><span data-stu-id="aea55-106">Contains DDE share attributes maintained by the NetDDE Share Database Manager (DSDM).</span></span> <span data-ttu-id="aea55-107">Дескриптор безопасности, связанный с каждым общим ресурсом DDE, не передается через эту структуру, но доступ к ним осуществляется с помощью конкретных функций.</span><span class="sxs-lookup"><span data-stu-id="aea55-107">The security descriptor associated with each DDE share is not passed through this structure but is accessed through specific functions.</span></span> <span data-ttu-id="aea55-108">API-интерфейс NetDDE DSDM принимает эту структуру для функций Set. для функций Get функция DSDM возвращает структуру, упакованную в предоставленный буфер, а также данные, на которые ссылаются члены **лпсзшаренаме**, **лпсзапптопиклист** и **лпсзитемлист**.</span><span class="sxs-lookup"><span data-stu-id="aea55-108">The NetDDE DSDM API accepts this structure for set functions; for get functions, the DSDM returns the structure packed into the supplied buffer along with the data referenced by the members **lpszShareName**, **lpszAppTopicList**, and **lpszItemList**.</span></span>

## <a name="syntax"></a><span data-ttu-id="aea55-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aea55-109">Syntax</span></span>


```C++
typedef struct _NDDESHAREINFO {
  LONG   lRevision;
  LPTSTR lpszShareName;
  LONG   lShareType;
  LPTSTR lpszAppTopicList;
  LONG   fSharedFlag;
  LONG   fService;
  LONG   fStartAppFlag;
  LONG   nCmdShow;
  LONG   qModifyId[2];
  LONG   cNumItems;
  LPTSTR lpszItemList;
} NDDESHAREINFO, *PNDDESHAREINFO;
```



## <a name="members"></a><span data-ttu-id="aea55-110">Члены</span><span class="sxs-lookup"><span data-stu-id="aea55-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="aea55-111">**лревисион**</span><span class="sxs-lookup"><span data-stu-id="aea55-111">**lRevision**</span></span>
</dt> <dd>

<span data-ttu-id="aea55-112">Уровень редакции структуры **нддешареинфо** .</span><span class="sxs-lookup"><span data-stu-id="aea55-112">The revision level of the **NDDESHAREINFO** structure.</span></span> <span data-ttu-id="aea55-113">В настоящее время уровень редакции равен 1.</span><span class="sxs-lookup"><span data-stu-id="aea55-113">Currently, the revision level is 1.</span></span>

</dd> <dt>

<span data-ttu-id="aea55-114">**лпсзшаренаме**</span><span class="sxs-lookup"><span data-stu-id="aea55-114">**lpszShareName**</span></span>
</dt> <dd>

<span data-ttu-id="aea55-115">Имя общей папки.</span><span class="sxs-lookup"><span data-stu-id="aea55-115">The name of the share.</span></span> <span data-ttu-id="aea55-116">Длина этой строки не должна превышать максимально \_ нддешаренаме символов.</span><span class="sxs-lookup"><span data-stu-id="aea55-116">This string must be no more than MAX\_NDDESHARENAME characters long.</span></span>

</dd> <dt>

<span data-ttu-id="aea55-117">**лшаретипе**</span><span class="sxs-lookup"><span data-stu-id="aea55-117">**lShareType**</span></span>
</dt> <dd>

<span data-ttu-id="aea55-118">Один или несколько типов общих ресурсов DDE.</span><span class="sxs-lookup"><span data-stu-id="aea55-118">One or more DDE share types.</span></span> <span data-ttu-id="aea55-119">Этот член может быть сочетанием следующих поддерживаемых типов общего ресурса DDE.</span><span class="sxs-lookup"><span data-stu-id="aea55-119">This member can be a combination of the following supported DDE share types.</span></span>



| <span data-ttu-id="aea55-120">Тип общего ресурса</span><span class="sxs-lookup"><span data-stu-id="aea55-120">Share type</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="aea55-121">Значение</span><span class="sxs-lookup"><span data-stu-id="aea55-121">Meaning</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SHARE_TYPE_NEW"></span><span id="share_type_new"></span><dl> <span data-ttu-id="aea55-122"><dt>**Общий доступ \_ Введите \_ Новый**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="aea55-122"><dt>**SHARE\_TYPE\_NEW**</dt> <dt>0x02</dt></span></span> </dl>          | <span data-ttu-id="aea55-123">Общая папка содержит пару "приложение — OLE" или "раздел".</span><span class="sxs-lookup"><span data-stu-id="aea55-123">The share contains an OLE application/topic pair.</span></span><br/>   |
| <span id="SHARE_TYPE_OLD"></span><span id="share_type_old"></span><dl> <span data-ttu-id="aea55-124"><dt>**Общий доступ \_ Введите \_ старый**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="aea55-124"><dt>**SHARE\_TYPE\_OLD**</dt> <dt>0x01</dt></span></span> </dl>          | <span data-ttu-id="aea55-125">Общая папка содержит пару "приложение-раздел" DDE.</span><span class="sxs-lookup"><span data-stu-id="aea55-125">The share contains a DDE application/topic pair.</span></span><br/>    |
| <span id="SHARE_TYPE_STATIC"></span><span id="share_type_static"></span><dl> <span data-ttu-id="aea55-126"><dt>**Общий доступ \_ Введите \_ статический**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="aea55-126"><dt>**SHARE\_TYPE\_STATIC**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="aea55-127">Общая папка содержит статическую пару "приложение-раздел".</span><span class="sxs-lookup"><span data-stu-id="aea55-127">The share contains a static application/topic pair.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="aea55-128">**лпсзапптопиклист**</span><span class="sxs-lookup"><span data-stu-id="aea55-128">**lpszAppTopicList**</span></span>
</dt> <dd>

<span data-ttu-id="aea55-129">Указатель на буфер, содержащий строки, заканчивающиеся нулем, для пар «DDE», «OLE» и «статическая тема приложения/раздела».</span><span class="sxs-lookup"><span data-stu-id="aea55-129">A pointer to a buffer containing null-terminated strings for the DDE, OLE, and static application/topic pairs.</span></span> <span data-ttu-id="aea55-130">Буфер должен иметь следующий формат:</span><span class="sxs-lookup"><span data-stu-id="aea55-130">The buffer should be in the following format:</span></span>

``` syntax
<DDE application name>|<DDE topic name>\0
<OLE application name>|<OLE topic name>\0
<static application name>|<static topic name>\0\0
```

</dd> <dt>

<span data-ttu-id="aea55-131">**фшаредфлаг**</span><span class="sxs-lookup"><span data-stu-id="aea55-131">**fSharedFlag**</span></span>
</dt> <dd>

<span data-ttu-id="aea55-132">Если этот член имеет **значение false**, общий ресурс DDE не позволит удаленным пользователям взаимодействовать через него с помощью DDE.</span><span class="sxs-lookup"><span data-stu-id="aea55-132">If this member is **FALSE**, the DDE share will not allow remote users to communicate through it by using DDE.</span></span> <span data-ttu-id="aea55-133">Однако локальные пользователи по-прежнему могут взаимодействовать через общий ресурс DDE.</span><span class="sxs-lookup"><span data-stu-id="aea55-133">However, local users can still communicate through the DDE share.</span></span> <span data-ttu-id="aea55-134">Ссылки на локальные клиенты всегда подразумеваются, если соответствующие списки DACL предоставляют доступ.</span><span class="sxs-lookup"><span data-stu-id="aea55-134">Local client links are always implied if the associated DACL grants access.</span></span>

</dd> <dt>

<span data-ttu-id="aea55-135">**фсервице**</span><span class="sxs-lookup"><span data-stu-id="aea55-135">**fService**</span></span>
</dt> <dd>

<span data-ttu-id="aea55-136">Если этот член задан, общий ресурс DDE не будет проверять, установлен ли этот пользователь как доверенный, прежде чем разрешить взаимодействие DDE.</span><span class="sxs-lookup"><span data-stu-id="aea55-136">If this member is set, the DDE share will not check whether the current user has set it as trusted before allowing DDE communication.</span></span>

</dd> <dt>

<span data-ttu-id="aea55-137">**фстартаппфлаг**</span><span class="sxs-lookup"><span data-stu-id="aea55-137">**fStartAppFlag**</span></span>
</dt> <dd>

<span data-ttu-id="aea55-138">Если этот элемент задан и общая папка является доверенной для запуска приложений, NetDDE попытается запустить приложение, указанное в **лпсзапптопиклист** , если не может изначально начать сеанс DDE с приложением.</span><span class="sxs-lookup"><span data-stu-id="aea55-138">If this member is set and the share is trusted to start applications, NetDDE will attempt to start the application specified by **lpszAppTopicList** if it cannot initially start a DDE conversation with the application.</span></span>

</dd> <dt>

<span data-ttu-id="aea55-139">**нкмдшов**</span><span class="sxs-lookup"><span data-stu-id="aea55-139">**nCmdShow**</span></span>
</dt> <dd>

<span data-ttu-id="aea55-140">Когда NetDDE запускает приложение для инициации диалога DDE, это значение отправляется в приложение с помощью параметра *нкмдшов* функции [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) .</span><span class="sxs-lookup"><span data-stu-id="aea55-140">When NetDDE starts an application to initiate a DDE conversation, this value is sent to the application through the *nCmdShow* parameter of the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function.</span></span> <span data-ttu-id="aea55-141">Он определяет предпочтительный режим отображения окна приложения в.</span><span class="sxs-lookup"><span data-stu-id="aea55-141">It defines the preferred mode for the application window to be shown in.</span></span> <span data-ttu-id="aea55-142">Этот параметр важен только в том случае, если **фстартаппфлаг** является активным.</span><span class="sxs-lookup"><span data-stu-id="aea55-142">This parameter is significant only if **fStartAppFlag** is active.</span></span> <span data-ttu-id="aea55-143">Пользователь, выполнивший вход в систему, в контексте которого запущено приложение, может также переопределить этот параметр при повышении общего ресурса до состояния доверия.</span><span class="sxs-lookup"><span data-stu-id="aea55-143">The logged on user in whose context the application is started can also override this option when promoting the share to trusted status.</span></span> <span data-ttu-id="aea55-144">Значение по умолчанию для этого элемента — SW \_ шовмаксимизед.</span><span class="sxs-lookup"><span data-stu-id="aea55-144">The default for this member is SW\_SHOWMAXIMIZED.</span></span>

</dd> <dt>

<span data-ttu-id="aea55-145">**кмодифид**</span><span class="sxs-lookup"><span data-stu-id="aea55-145">**qModifyId**</span></span>
</dt> <dd>

<span data-ttu-id="aea55-146">8-байтовый серийный номер, указывающий серийный номер изменения общего ресурса DDE.</span><span class="sxs-lookup"><span data-stu-id="aea55-146">An 8-byte serial number that indicates the modification serial number of the DDE share.</span></span> <span data-ttu-id="aea55-147">Каждый раз, когда общий ресурс DDE изменяется вызовом [**нддешаресетинфо**](nddesharesetinfo.md) или [**нддесетшаресекурити**](nddesetsharesecurity.md) , эти значения изменяются.</span><span class="sxs-lookup"><span data-stu-id="aea55-147">Every time the DDE share is modified by a [**NDdeShareSetInfo**](nddesharesetinfo.md) or [**NDdeSetShareSecurity**](nddesetsharesecurity.md) call, these values are changed.</span></span>

</dd> <dt>

<span data-ttu-id="aea55-148">**кнумитемс**</span><span class="sxs-lookup"><span data-stu-id="aea55-148">**cNumItems**</span></span>
</dt> <dd>

<span data-ttu-id="aea55-149">Число элементов, перечисленных в **лпсзитемлист**.</span><span class="sxs-lookup"><span data-stu-id="aea55-149">The number of items listed in **lpszItemList**.</span></span> <span data-ttu-id="aea55-150">Если **кнумитемс** равен нулю, то **лпсзитемлист** является пустым, а сведения об общем ресурсе и связанном дескрипторе безопасности применяются ко всем элементам, обслуживаемым связанным приложением.</span><span class="sxs-lookup"><span data-stu-id="aea55-150">If **cNumItems** is zero, then **lpszItemList** is empty, and the share information and associated security descriptor apply to all items serviced by the associated application.</span></span>

</dd> <dt>

<span data-ttu-id="aea55-151">**лпсзитемлист**</span><span class="sxs-lookup"><span data-stu-id="aea55-151">**lpszItemList**</span></span>
</dt> <dd>

<span data-ttu-id="aea55-152">Указатель на буфер, содержащий строки, заканчивающиеся нулем, указывающие элементы, которые клиентское приложение в транзакции DDE может запрашивать или запускать циклы Advise.</span><span class="sxs-lookup"><span data-stu-id="aea55-152">A pointer to a buffer containing null-terminated strings that specify the items the client application in a DDE transaction can request or start advise loops on.</span></span> <span data-ttu-id="aea55-153">Если в списке нет элементов, общий ресурс DDE позволяет использовать любой элемент.</span><span class="sxs-lookup"><span data-stu-id="aea55-153">If no items are listed, the DDE share allows any item to be used.</span></span> <span data-ttu-id="aea55-154">Число элементов в списке должно соответствовать количеству **кнумитемс** .</span><span class="sxs-lookup"><span data-stu-id="aea55-154">The number of items in the list must match the **cNumItems** count.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aea55-155">Требования</span><span class="sxs-lookup"><span data-stu-id="aea55-155">Requirements</span></span>



| <span data-ttu-id="aea55-156">Требование</span><span class="sxs-lookup"><span data-stu-id="aea55-156">Requirement</span></span> | <span data-ttu-id="aea55-157">Значение</span><span class="sxs-lookup"><span data-stu-id="aea55-157">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aea55-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aea55-158">Minimum supported client</span></span><br/> | <span data-ttu-id="aea55-159">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aea55-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="aea55-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aea55-160">Minimum supported server</span></span><br/> | <span data-ttu-id="aea55-161">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aea55-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="aea55-162">Заголовок</span><span class="sxs-lookup"><span data-stu-id="aea55-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="aea55-163"><dt>Нддеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="aea55-163"><dt>Nddeapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aea55-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aea55-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aea55-165">Общие сведения о сетевом платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="aea55-165">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="aea55-166">Структуры сетевого DDE</span><span class="sxs-lookup"><span data-stu-id="aea55-166">Network DDE Structures</span></span>](network-dde-structures.md)
</dt> <dt>

[<span data-ttu-id="aea55-167">**нддесетшаресекурити**</span><span class="sxs-lookup"><span data-stu-id="aea55-167">**NDdeSetShareSecurity**</span></span>](nddesetsharesecurity.md)
</dt> <dt>

[<span data-ttu-id="aea55-168">**нддешаресетинфо**</span><span class="sxs-lookup"><span data-stu-id="aea55-168">**NDdeShareSetInfo**</span></span>](nddesharesetinfo.md)
</dt> <dt>

[<span data-ttu-id="aea55-169">**WinMain**</span><span class="sxs-lookup"><span data-stu-id="aea55-169">**WinMain**</span></span>](/windows/win32/api/winbase/nf-winbase-winmain)
</dt> </dl>

 

