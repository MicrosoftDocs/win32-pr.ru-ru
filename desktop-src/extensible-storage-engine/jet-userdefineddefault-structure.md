---
description: 'Дополнительные сведения: структура JET_USERDEFINEDDEFAULT'
title: Структура JET_USERDEFINEDDEFAULT
TOCTitle: JET_USERDEFINEDDEFAULT Structure
ms:assetid: 1f0a5419-9fae-4a93-a271-2f9772ecc996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269200(v=EXCHG.10)
ms:contentKeyID: 32765503
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5f588588a1a6769e997264321f8911a86e169c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693580"
---
# <a name="jet_userdefineddefault-structure"></a><span data-ttu-id="01b7c-103">Структура JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="01b7c-103">JET_USERDEFINEDDEFAULT Structure</span></span>


<span data-ttu-id="01b7c-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="01b7c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_userdefineddefault-structure"></a><span data-ttu-id="01b7c-105">Структура JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="01b7c-105">JET_USERDEFINEDDEFAULT Structure</span></span>

<span data-ttu-id="01b7c-106">Структура **JET_USERDEFINEDDEFAULT** задается вместе с JET_bitColumnUserDefinedDefault, чтобы дать новому столбцу значение по умолчанию, которое определяется с помощью обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="01b7c-106">The **JET_USERDEFINEDDEFAULT** structure is specified in conjunction with JET_bitColumnUserDefinedDefault to give a new column a default value that is determined using a callback.</span></span> <span data-ttu-id="01b7c-107">Этот метод можно использовать для реализации вычисленных столбцов.</span><span class="sxs-lookup"><span data-stu-id="01b7c-107">This technique can be used to implement computed columns.</span></span>

<span data-ttu-id="01b7c-108">**Windows XP:** Структура **JET_USERDEFINEDDEFAULT** появилась в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="01b7c-108">**Windows XP:** The **JET_USERDEFINEDDEFAULT** structure is introduced in Windows XP.</span></span>

```cpp
    typedef struct tag_JET_USERDEFINEDDEFAULT {
      tchar* szCallback;
      unsigned char* pbUserData;
      unsigned long cbUserData;
      tchar* szDependantColumns;
    } JET_USERDEFINEDDEFAULT;
```

### <a name="members"></a><span data-ttu-id="01b7c-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="01b7c-109">Members</span></span>

<span data-ttu-id="01b7c-110">**сзкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="01b7c-110">**szCallback**</span></span>

<span data-ttu-id="01b7c-111">Имя экспорта функции, реализующей обратный вызов в формате "функция модуля \! ".</span><span class="sxs-lookup"><span data-stu-id="01b7c-111">The export name of the function that implements the callback in "module\!function" format.</span></span>

<span data-ttu-id="01b7c-112">Обратный вызов сохраняется как часть схемы столбца.</span><span class="sxs-lookup"><span data-stu-id="01b7c-112">The callback persists as a part of the column schema.</span></span> <span data-ttu-id="01b7c-113">Фактический исполняемый файл узла и имя экспорта функции должны сохраняться для включения поиска действительного адреса функции во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="01b7c-113">The actual host executable and export name of the function must persist to enable the lookup of the true address of the function at run time.</span></span>

<span data-ttu-id="01b7c-114">Имя модуля — это имя двоичного файла узла, содержащего функцию.</span><span class="sxs-lookup"><span data-stu-id="01b7c-114">The module name is the name of the host binary that contains the function.</span></span> <span data-ttu-id="01b7c-115">Имя функции — это имя экспорта для этой функции.</span><span class="sxs-lookup"><span data-stu-id="01b7c-115">The function name is the name of the export for that function.</span></span> <span data-ttu-id="01b7c-116">Эти два фрагмента информации будут использоваться ядром СУБД в среде выполнения для поиска действительного адреса обратного вызова путем выполнения вызова [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) для имени модуля, за которым следует вызов [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) в имени функции.</span><span class="sxs-lookup"><span data-stu-id="01b7c-116">These two pieces of information will be used by the database engine at runtime to locate the true address of the callback by executing a [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) call on the module name followed by a [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) call on the function name.</span></span>

<span data-ttu-id="01b7c-117">Например, если обратный вызов был реализован в библиотеке DLL с именем MyCallback.DLL и эта библиотека DLL хранилась в C: \\ MyApplication, а функция, реализующая обратный вызов, была экспортирована из библиотеки DLL как усердефинеддефаулткаллбакк, то необходимая строка будет иметь вид "C: \\ MyApplication \\MyCallback.DLL\! усердефинеддефаулткаллбакк".</span><span class="sxs-lookup"><span data-stu-id="01b7c-117">For example, if the callback were implemented in a DLL called MyCallback.DLL and that DLL were stored in C:\\MyApplication and the function implementing the callback were exported from the DLL as UserDefinedDefaultCallback, then the required string would be "C:\\MyApplication\\MyCallback.DLL\!UserDefinedDefaultCallback".</span></span>

<span data-ttu-id="01b7c-118">**Примечание**  .  Внедренный " \! "</span><span class="sxs-lookup"><span data-stu-id="01b7c-118">**Note**  Embedded "\!"</span></span> <span data-ttu-id="01b7c-119">символы в части модуля имени обратного вызова не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="01b7c-119">characters in the module portion of the callback name are not supported.</span></span>

<span data-ttu-id="01b7c-120">Настоятельно рекомендуется использовать имя обратного вызова, которое не является функцией архитектуры узла.</span><span class="sxs-lookup"><span data-stu-id="01b7c-120">It is highly recommended that you use a callback name that is not a function of the host architecture.</span></span> <span data-ttu-id="01b7c-121">Например, не используйте экспорты, объявленные как STDCALL ( UserDefinedDefaultCallback@32 ), так как это соглашение о вызовах поддерживается только на компьютерах x86.</span><span class="sxs-lookup"><span data-stu-id="01b7c-121">For example, do not use exports decorated as stdcall (UserDefinedDefaultCallback@32) because this calling convention is only supported on x86 machines.</span></span> <span data-ttu-id="01b7c-122">При использовании такого обратного вызова базу данных можно было использовать только на компьютере x86.</span><span class="sxs-lookup"><span data-stu-id="01b7c-122">If such a callback were used then the database could only be used on an x86 machine.</span></span> <span data-ttu-id="01b7c-123">В этом случае необходимо использовать псевдоним, чтобы сделать независимым от платформы экспорт.</span><span class="sxs-lookup"><span data-stu-id="01b7c-123">An alias should be used to make a platform-agnostic export in this case.</span></span>

<span data-ttu-id="01b7c-124">Настоятельно рекомендуется использовать полный путь к имени модуля, реализующего обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="01b7c-124">It is highly recommended that you use the full path of the module name that is implementing the callback.</span></span> <span data-ttu-id="01b7c-125">Если используется относительный путь, процесс, в котором размещается база данных, может быть уязвим для атаки с помощью мошеннического двоичного файла.</span><span class="sxs-lookup"><span data-stu-id="01b7c-125">If a relative path is used then the process that is hosting the database might be susceptible to attack by a rogue binary.</span></span>

<span data-ttu-id="01b7c-126">Приложение должно передавать ядру СУБД только доверенные обратные вызовы.</span><span class="sxs-lookup"><span data-stu-id="01b7c-126">The application should pass only trusted callbacks to the database engine.</span></span> <span data-ttu-id="01b7c-127">Ядро СУБД загрузит двоичный файл, чтобы проверить его существование при создании связанного столбца.</span><span class="sxs-lookup"><span data-stu-id="01b7c-127">The database engine will load the binary to verify its existence when the associated column is created.</span></span> <span data-ttu-id="01b7c-128">Если путь к двоичному файлу не проверен или является доверенным, он может атаковать процесс, в котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="01b7c-128">If the path to the binary is not validated or known to be trusted then it could attack the process that is hosting the database.</span></span>

<span data-ttu-id="01b7c-129">**пбусердата**</span><span class="sxs-lookup"><span data-stu-id="01b7c-129">**pbUserData**</span></span>

<span data-ttu-id="01b7c-130">Автономный блок определяемых пользователем данных, передаваемый обратному вызову при вызове. Предоставленный блок данных будет сохранен как часть схемы столбца.</span><span class="sxs-lookup"><span data-stu-id="01b7c-130">A self-contained block of user-defined data to be passed to the callback when invoked.The data block that is provided will persist as a part of the column schema.</span></span> <span data-ttu-id="01b7c-131">В результате блок данных должен быть полностью автономным и не может ссылаться на данные, находящиеся за пределами области базы данных.</span><span class="sxs-lookup"><span data-stu-id="01b7c-131">As a result, the data block must be entirely self-contained and cannot refer to any data that is outside the scope of the database.</span></span>

<span data-ttu-id="01b7c-132">Если **пбусердата** равен нулю, значение **cbUserData** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="01b7c-132">If **pbUserData** is zero then the value of **cbUserData** is ignored.</span></span> <span data-ttu-id="01b7c-133">В этом случае при вызове функции обратного вызова не будут переданы пользовательские данные.</span><span class="sxs-lookup"><span data-stu-id="01b7c-133">In this case, no user-defined data will be passed to the callback when invoked.</span></span>

<span data-ttu-id="01b7c-134">**cbUserData**</span><span class="sxs-lookup"><span data-stu-id="01b7c-134">**cbUserData**</span></span>

<span data-ttu-id="01b7c-135">См. **пбусердата**.</span><span class="sxs-lookup"><span data-stu-id="01b7c-135">See **pbUserData**.</span></span>

<span data-ttu-id="01b7c-136">**сздепендантколумнс**</span><span class="sxs-lookup"><span data-stu-id="01b7c-136">**szDependantColumns**</span></span>

<span data-ttu-id="01b7c-137">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="01b7c-137">Reserved for future use.</span></span>

<span data-ttu-id="01b7c-138">Этот элемент всегда должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="01b7c-138">This member should always be set to NULL.</span></span>

### <a name="requirements"></a><span data-ttu-id="01b7c-139">Требования</span><span class="sxs-lookup"><span data-stu-id="01b7c-139">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01b7c-140"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="01b7c-140"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="01b7c-141">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="01b7c-141">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01b7c-142"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="01b7c-142"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="01b7c-143">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="01b7c-143">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01b7c-144"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="01b7c-144"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="01b7c-145">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="01b7c-145">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01b7c-146"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="01b7c-146"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="01b7c-147">Реализуется как <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Юникод) и <strong>JET_ USERDEFINEDDEFAULT_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="01b7c-147">Implemented as <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Unicode) and <strong>JET_ USERDEFINEDDEFAULT_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="01b7c-148">См. также:</span><span class="sxs-lookup"><span data-stu-id="01b7c-148">See Also</span></span>

[<span data-ttu-id="01b7c-149">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="01b7c-149">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="01b7c-150">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="01b7c-150">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="01b7c-151">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="01b7c-151">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)
