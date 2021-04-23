---
description: Уведомление СПФИЛЕНОТИФИ \_ лангмисматч отправляется в подпрограммы обратного вызова, если язык копируемого файла не совпадает с языком существующего целевого файла.
ms.assetid: dff3969e-5847-4ad5-b7d4-237144bbe8e6
title: Сообщение SPFILENOTIFY_LANGMISMATCH (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3d7828c90dd4dabb8e1cb73a8dcca7ae33ebd3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664456"
---
# <a name="spfilenotify_langmismatch-message"></a><span data-ttu-id="e2219-103">\_Сообщение спфиленотифи лангмисматч</span><span class="sxs-lookup"><span data-stu-id="e2219-103">SPFILENOTIFY\_LANGMISMATCH message</span></span>

<span data-ttu-id="e2219-104">Уведомление **спфиленотифи \_ лангмисматч** отправляется в подпрограммы обратного вызова, если язык копируемого файла не совпадает с языком существующего целевого файла.</span><span class="sxs-lookup"><span data-stu-id="e2219-104">The **SPFILENOTIFY\_LANGMISMATCH** notification is sent to the callback routine if the language of the file to be copied does not match the language of an existing target file.</span></span> <span data-ttu-id="e2219-105">Его можно отправить в подпрограммы обратного вызова отдельно или вместе с помощью оператора OR с [**спфиленотифи \_ таржетексистс**](spfilenotify-targetexists.md) и/или [**спфиленотифи \_ таржетневер**](spfilenotify-targetnewer.md).</span><span class="sxs-lookup"><span data-stu-id="e2219-105">It can be sent to the callback routine alone or combined, by using the OR operator, with [**SPFILENOTIFY\_TARGETEXISTS**](spfilenotify-targetexists.md) and/or [**SPFILENOTIFY\_TARGETNEWER**](spfilenotify-targetnewer.md).</span></span>


```C++
SPFILENOTIFY_LANGMISMATCH
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) LanguageInfo;
            
```



## <a name="parameters"></a><span data-ttu-id="e2219-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2219-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2219-107">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="e2219-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="e2219-108">Указатель на структуру [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) , содержащую сведения о путях к исходному и целевому файлам.</span><span class="sxs-lookup"><span data-stu-id="e2219-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains information about the paths of the source and target files.</span></span>

</dd> <dt>

<span data-ttu-id="e2219-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="e2219-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="e2219-110">Определяет несоответствующие языки.</span><span class="sxs-lookup"><span data-stu-id="e2219-110">Identifies the mismatched languages.</span></span> <span data-ttu-id="e2219-111">Этот элемент имеет идентификатор языка исходного файла в нижнем слове и идентификатор языка существующего целевого файла в верхнем слове.</span><span class="sxs-lookup"><span data-stu-id="e2219-111">This member has the language identifier of the source file in the low word, and the language identifier of the existing target file in the high word.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2219-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2219-112">Return value</span></span>

<span data-ttu-id="e2219-113">Подпрограммы обратного вызова должны возвращать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e2219-113">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="e2219-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e2219-114">Return code</span></span>                                                                          | <span data-ttu-id="e2219-115">Описание</span><span class="sxs-lookup"><span data-stu-id="e2219-115">Description</span></span>                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e2219-116"><dt>**УСЛОВИЯ**</dt></span><span class="sxs-lookup"><span data-stu-id="e2219-116"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="e2219-117">Скопируйте файл и Перезапишите существующий файл.</span><span class="sxs-lookup"><span data-stu-id="e2219-117">Copy the file and overwrite the existing file.</span></span><br/>               |
| <dl> <span data-ttu-id="e2219-118"><dt>**ISFALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="e2219-118"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="e2219-119">Пропустить операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="e2219-119">Skip the copy operation.</span></span> <span data-ttu-id="e2219-120">Не перезаписывайте существующий файл.</span><span class="sxs-lookup"><span data-stu-id="e2219-120">Do not overwrite the existing file.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e2219-121">Требования</span><span class="sxs-lookup"><span data-stu-id="e2219-121">Requirements</span></span>



| <span data-ttu-id="e2219-122">Требование</span><span class="sxs-lookup"><span data-stu-id="e2219-122">Requirement</span></span> | <span data-ttu-id="e2219-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e2219-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2219-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2219-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e2219-125">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e2219-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e2219-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2219-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e2219-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e2219-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2219-128">Header</span><span class="sxs-lookup"><span data-stu-id="e2219-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2219-129"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2219-129"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2219-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2219-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2219-131">Обзор</span><span class="sxs-lookup"><span data-stu-id="e2219-131">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="e2219-132">Уведомления</span><span class="sxs-lookup"><span data-stu-id="e2219-132">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="e2219-133">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="e2219-133">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="e2219-134">**сетупкоммитфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="e2219-134">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="e2219-135">**сетупдефаулткуеуекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="e2219-135">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="e2219-136">**сетупинсталлфиле**</span><span class="sxs-lookup"><span data-stu-id="e2219-136">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="e2219-137">**сетупинсталлфиликс**</span><span class="sxs-lookup"><span data-stu-id="e2219-137">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="e2219-138">**сетупинсталлфроминфсектион**</span><span class="sxs-lookup"><span data-stu-id="e2219-138">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




