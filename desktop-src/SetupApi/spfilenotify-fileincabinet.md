---
description: Уведомление СПФИЛЕНОТИФИ \_ филеинкабинет отправляется в подпрограммы обратного вызова с помощью сетупитератекабинет для каждого файла, найденного в CAB-файле. Подпрограммы обратного вызова должны возвращать значение, указывающее, следует ли извлекать файл.
ms.assetid: c6d89759-c0d4-4741-b992-43eaa0dc4f01
title: Сообщение SPFILENOTIFY_FILEINCABINET (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496db3cef814f2bf366f4cb6f91132efe01a2406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664523"
---
# <a name="spfilenotify_fileincabinet-message"></a><span data-ttu-id="fcc12-104">\_Сообщение спфиленотифи филеинкабинет</span><span class="sxs-lookup"><span data-stu-id="fcc12-104">SPFILENOTIFY\_FILEINCABINET message</span></span>

<span data-ttu-id="fcc12-105">Уведомление **спфиленотифи \_ филеинкабинет** отправляется в подпрограммы обратного вызова с помощью [**сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) для каждого файла, найденного в CAB-файле.</span><span class="sxs-lookup"><span data-stu-id="fcc12-105">The **SPFILENOTIFY\_FILEINCABINET** notification is sent to a callback routine by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) for each file found in the cabinet.</span></span> <span data-ttu-id="fcc12-106">Подпрограммы обратного вызова должны возвращать значение, указывающее, следует ли извлекать файл.</span><span class="sxs-lookup"><span data-stu-id="fcc12-106">The callback routine must return a value indicating whether to extract the file.</span></span>


```C++
SPFILENOTIFY_FILEINCABINET
  Param1 = (UINT) FileInCabinetInfo;
  Param2 = (UINT) CabinetFile;
            
```



## <a name="parameters"></a><span data-ttu-id="fcc12-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fcc12-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcc12-108">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="fcc12-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="fcc12-109">Указатель на [**файл \_ в \_ \_ информационной структуре CAB**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) -файла, содержащий сведения о файле из CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="fcc12-109">Pointer to a [**FILE\_IN\_CABINET\_INFO**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) structure that contains information about the file in the cabinet.</span></span>

</dd> <dt>

<span data-ttu-id="fcc12-110">*Param2*</span><span class="sxs-lookup"><span data-stu-id="fcc12-110">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="fcc12-111">Указатель на строку, завершающуюся нулем, которая содержит имя файла CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="fcc12-111">Pointer to a null-terminated string that contains the filename of the cabinet file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcc12-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fcc12-112">Return value</span></span>

<span data-ttu-id="fcc12-113">Подпрограммы обратного вызова должны возвращать одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="fcc12-113">Your callback routine should return one of the following.</span></span>



| <span data-ttu-id="fcc12-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fcc12-114">Return code</span></span>                                                                                 | <span data-ttu-id="fcc12-115">Описание</span><span class="sxs-lookup"><span data-stu-id="fcc12-115">Description</span></span>                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="fcc12-116"><dt>**ФИЛЕОП \_ пропустить**</dt></span><span class="sxs-lookup"><span data-stu-id="fcc12-116"><dt>**FILEOP\_SKIP**</dt></span></span> </dl> | <span data-ttu-id="fcc12-117">Не извлекайте файл, пропустите его.</span><span class="sxs-lookup"><span data-stu-id="fcc12-117">Do not extract the file, skip it.</span></span><br/> |
| <dl> <span data-ttu-id="fcc12-118"><dt>**ФИЛЕОП \_ доит**</dt></span><span class="sxs-lookup"><span data-stu-id="fcc12-118"><dt>**FILEOP\_DOIT**</dt></span></span> </dl> | <span data-ttu-id="fcc12-119">Извлеките файл.</span><span class="sxs-lookup"><span data-stu-id="fcc12-119">Extract the file.</span></span><br/>                 |



 

<span data-ttu-id="fcc12-120">Если подпрограммы обратного вызова возвращают ФИЛЕОП \_ доит, то имя, используемое для извлеченного файла, должно быть указано в **фуллтаржетнаме** члене [**файла \_ в структуре \_ \_ сведений о CAB-файле**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) , переданном в подпрограммы в параметре *param1*.</span><span class="sxs-lookup"><span data-stu-id="fcc12-120">If your callback routine returns FILEOP\_DOIT, the name to use for the extracted file should be specified in the **FullTargetName** member of the [**FILE\_IN\_CABINET\_INFO**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) structure passed to the routine in *Param1*.</span></span>

> [!Note]  
> <span data-ttu-id="fcc12-121">Нет подпрограммы обратного вызова CAB-файла по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fcc12-121">There is no default cabinet callback routine.</span></span> <span data-ttu-id="fcc12-122">Приложение установки должно предоставить подпрограммы обратного вызова для управления уведомлениями, отправленными [**сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="fcc12-122">The setup application should supply a callback routine to handle the notifications sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fcc12-123">Требования</span><span class="sxs-lookup"><span data-stu-id="fcc12-123">Requirements</span></span>



| <span data-ttu-id="fcc12-124">Требование</span><span class="sxs-lookup"><span data-stu-id="fcc12-124">Requirement</span></span> | <span data-ttu-id="fcc12-125">Значение</span><span class="sxs-lookup"><span data-stu-id="fcc12-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fcc12-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fcc12-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fcc12-127">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fcc12-127">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fcc12-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fcc12-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fcc12-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fcc12-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fcc12-130">Header</span><span class="sxs-lookup"><span data-stu-id="fcc12-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcc12-131"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcc12-131"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcc12-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fcc12-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcc12-133">Обзор</span><span class="sxs-lookup"><span data-stu-id="fcc12-133">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="fcc12-134">Уведомления</span><span class="sxs-lookup"><span data-stu-id="fcc12-134">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="fcc12-135">**ФАЙЛ \_ в \_ \_ сведениях о CAB-файле**</span><span class="sxs-lookup"><span data-stu-id="fcc12-135">**FILE\_IN\_CABINET\_INFO**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a)
</dt> <dt>

[<span data-ttu-id="fcc12-136">**сетупитератекабинет**</span><span class="sxs-lookup"><span data-stu-id="fcc12-136">**SetupIterateCabinet**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

 




