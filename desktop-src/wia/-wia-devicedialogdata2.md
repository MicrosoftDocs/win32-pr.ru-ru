---
description: Структура DEVICEDIALOGDATA2 — определяет данные, необходимые для вызова диалогового окна устройства.
ms.assetid: 544238de-310f-4fc3-b519-bb4e6b309272
title: Структура DEVICEDIALOGDATA2 (Виадефд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA2
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: 82ca6cba81101e577eed882ad45272ab81546fed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089811"
---
# <a name="devicedialogdata2-structure"></a><span data-ttu-id="090a8-103">Структура DEVICEDIALOGDATA2</span><span class="sxs-lookup"><span data-stu-id="090a8-103">DEVICEDIALOGDATA2 structure</span></span>

<span data-ttu-id="090a8-104">Определяет данные, необходимые для вызова диалогового окна устройства.</span><span class="sxs-lookup"><span data-stu-id="090a8-104">Defines the data needed to call a device dialog.</span></span>

## <a name="syntax"></a><span data-ttu-id="090a8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="090a8-105">Syntax</span></span>


```C++
typedef struct {
  DWORD     cbSize;
  IWiaItem2 *pIWiaItemRoot;
  DWORD     dwFlags;
  HWND      hwndParent;
  BSTR      bstrFolderName;
  BSTR      bstrFilename;
  LONG      lNumFiles;
  BSTR      *pbstrFilePaths;
  IWiaItem2 *ppWiaItem;
} DEVICEDIALOGDATA2;
```



## <a name="members"></a><span data-ttu-id="090a8-106">Члены</span><span class="sxs-lookup"><span data-stu-id="090a8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="090a8-107">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="090a8-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="090a8-108">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="090a8-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="090a8-109">Задает размер этой структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="090a8-109">Specifies the size of this structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="090a8-110">**пивиаитемрут**</span><span class="sxs-lookup"><span data-stu-id="090a8-110">**pIWiaItemRoot**</span></span>
</dt> <dd>

<span data-ttu-id="090a8-111">Тип: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***</span><span class="sxs-lookup"><span data-stu-id="090a8-111">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="090a8-112">Указывает на интерфейс [**IWiaItem2**](-wia-iwiaitem2.md) , представляющий допустимый корневой элемент в дереве элементов приложения.</span><span class="sxs-lookup"><span data-stu-id="090a8-112">Points to an [**IWiaItem2**](-wia-iwiaitem2.md) interface that represents the valid root item in the application item tree.</span></span>

</dd> <dt>

<span data-ttu-id="090a8-113">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="090a8-113">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="090a8-114">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="090a8-114">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="090a8-115">Задает набор флагов, управляющих работой диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="090a8-115">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="090a8-116">Можно задать любое из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="090a8-116">Can be set to any of the following values:</span></span>



| <span data-ttu-id="090a8-117">Flag</span><span class="sxs-lookup"><span data-stu-id="090a8-117">Flag</span></span>                                 | <span data-ttu-id="090a8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="090a8-118">Meaning</span></span>                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="090a8-119">0</span><span class="sxs-lookup"><span data-stu-id="090a8-119">0</span></span>                                    | <span data-ttu-id="090a8-120">Поведение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="090a8-120">Default behavior.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="090a8-121">\_ \_ \_ одиночное изображение диалогового окна WIA устройства \_</span><span class="sxs-lookup"><span data-stu-id="090a8-121">WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE</span></span>   | <span data-ttu-id="090a8-122">Ограничить выбор изображения одним изображением в диалоговом окне "получение образа устройства".</span><span class="sxs-lookup"><span data-stu-id="090a8-122">Restrict image selection to a single image in the device image acquisition dialog box.</span></span>                                                                                                      |
| <span data-ttu-id="090a8-123">\_ \_ \_ \_ Общий \_ Пользовательский интерфейс диалогового окна устройства WIA</span><span class="sxs-lookup"><span data-stu-id="090a8-123">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="090a8-124">Используйте пользовательский интерфейс системы, если он доступен, а не пользовательский интерфейс, предоставляемый поставщиком.</span><span class="sxs-lookup"><span data-stu-id="090a8-124">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="090a8-125">Если пользовательский интерфейс системы недоступен, используется пользовательский интерфейс поставщика.</span><span class="sxs-lookup"><span data-stu-id="090a8-125">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="090a8-126">Если ни один из ИНТЕРФЕЙСов не доступен, функция возвращает E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="090a8-126">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="090a8-127">**хвндпарент**</span><span class="sxs-lookup"><span data-stu-id="090a8-127">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="090a8-128">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="090a8-128">Type: **HWND**</span></span>

</dd> <dd>

<span data-ttu-id="090a8-129">Задает маркер родительского окна диалога.</span><span class="sxs-lookup"><span data-stu-id="090a8-129">Specifies the handle to the parent window of the dialog.</span></span>

</dd> <dt>

<span data-ttu-id="090a8-130">**бстрфолдернаме**</span><span class="sxs-lookup"><span data-stu-id="090a8-130">**bstrFolderName**</span></span>
</dt> <dd>

<span data-ttu-id="090a8-131">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="090a8-131">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="090a8-132">Указывает имя папки, в которую передаются файлы.</span><span class="sxs-lookup"><span data-stu-id="090a8-132">Specifies the folder name where the files are transferred.</span></span>

</dd> <dt>

<span data-ttu-id="090a8-133">**бстрфиленаме**</span><span class="sxs-lookup"><span data-stu-id="090a8-133">**bstrFilename**</span></span>
</dt> <dd>

<span data-ttu-id="090a8-134">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="090a8-134">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="090a8-135">Указывает шаблон имени файла, который будет использоваться для файлов, передаваемых из элементов WIA в целевую папку, назначенную **бстрфолдернаме**.</span><span class="sxs-lookup"><span data-stu-id="090a8-135">Specifies the filename template to be used for files transferred from WIA items to the destination folder designated by **bstrFolderName**.</span></span> <span data-ttu-id="090a8-136">Можно создать произвольное число уникальных имен файлов, добавив дополнительные символы в шаблон имени файла.</span><span class="sxs-lookup"><span data-stu-id="090a8-136">An arbitrary number of unique file names can be created by appending additional characters to the file name template.</span></span>

</dd> <dt>

<span data-ttu-id="090a8-137">**лнумфилес**</span><span class="sxs-lookup"><span data-stu-id="090a8-137">**lNumFiles**</span></span>
</dt> <dd>

<span data-ttu-id="090a8-138">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="090a8-138">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="090a8-139">Получает число строк, записанных в массив **пбстрфилепасс** .</span><span class="sxs-lookup"><span data-stu-id="090a8-139">Receives the number of strings written to the **pbstrFilePaths** array.</span></span>

</dd> <dt>

<span data-ttu-id="090a8-140">**пбстрфилепасс**</span><span class="sxs-lookup"><span data-stu-id="090a8-140">**pbstrFilePaths**</span></span>
</dt> <dd>

<span data-ttu-id="090a8-141">Тип: **BSTR \***</span><span class="sxs-lookup"><span data-stu-id="090a8-141">Type: **BSTR\***</span></span>

</dd> <dd>

<span data-ttu-id="090a8-142">Указатель на массив указателей BSTR.</span><span class="sxs-lookup"><span data-stu-id="090a8-142">Pointer to an array of BSTR pointers.</span></span> <span data-ttu-id="090a8-143">Каждый элемент массива указывает на BSTR, содержащий целевое имя файла, который был успешно передан в папку, определенную параметром Бстрфолдернаме.</span><span class="sxs-lookup"><span data-stu-id="090a8-143">Each array element points to a BSTR that contains the destination name of a file that was successfully transferred to the folder identified by bstrFolderName.</span></span> <span data-ttu-id="090a8-144">Метод должен выделить хранилище для этого элемента.</span><span class="sxs-lookup"><span data-stu-id="090a8-144">The method must allocate the storage for this member.</span></span>

</dd> <dt>

<span data-ttu-id="090a8-145">**ппвиаитем**</span><span class="sxs-lookup"><span data-stu-id="090a8-145">**ppWiaItem**</span></span>
</dt> <dd>

<span data-ttu-id="090a8-146">Тип: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***</span><span class="sxs-lookup"><span data-stu-id="090a8-146">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="090a8-147">Указатель на интерфейс [**IWiaItem2**](-wia-iwiaitem2.md) элемента WIA, который передает данные в файл или файлы, имена которых находятся в массиве **пбстрфилепасс** .</span><span class="sxs-lookup"><span data-stu-id="090a8-147">Pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the WIA item that transfers data to the file or files named in the **pbstrFilePaths** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="090a8-148">Требования</span><span class="sxs-lookup"><span data-stu-id="090a8-148">Requirements</span></span>



| <span data-ttu-id="090a8-149">Требование</span><span class="sxs-lookup"><span data-stu-id="090a8-149">Requirement</span></span> | <span data-ttu-id="090a8-150">Значение</span><span class="sxs-lookup"><span data-stu-id="090a8-150">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="090a8-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="090a8-151">Minimum supported client</span></span><br/> | <span data-ttu-id="090a8-152">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="090a8-152">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="090a8-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="090a8-153">Minimum supported server</span></span><br/> | <span data-ttu-id="090a8-154">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="090a8-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="090a8-155">Header</span><span class="sxs-lookup"><span data-stu-id="090a8-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="090a8-156"><dt>Виадефд. h</dt></span><span class="sxs-lookup"><span data-stu-id="090a8-156"><dt>Wiadefd.h</dt></span></span> </dl> |



 

 




