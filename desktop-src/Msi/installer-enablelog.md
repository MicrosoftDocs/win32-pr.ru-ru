---
description: Метод EnableLog объекта Installer позволяет вести журнал выбранного типа сообщений для всех последующих сеансов установки в пространстве текущего процесса.
ms.assetid: eb384587-0870-4812-866c-b483c1dfa841
title: Метод Installer. EnableLog
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.EnableLog
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 573b56dda0479f58595b0849f6443fd8a2e67e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651627"
---
# <a name="installerenablelog-method"></a><span data-ttu-id="b0058-103">Метод Installer. EnableLog</span><span class="sxs-lookup"><span data-stu-id="b0058-103">Installer.EnableLog method</span></span>

<span data-ttu-id="b0058-104">Метод **EnableLog** объекта [**Installer**](installer-object.md) позволяет вести журнал выбранного типа сообщений для всех последующих сеансов установки в пространстве текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="b0058-104">The **EnableLog** method of the [**Installer**](installer-object.md) object enables logging of the selected message type for all subsequent installation sessions in the current process space.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0058-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0058-105">Syntax</span></span>


```JScript
Installer.EnableLog(
  logMode,
  logFile
)
```



## <a name="parameters"></a><span data-ttu-id="b0058-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0058-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0058-107">*logMode*</span><span class="sxs-lookup"><span data-stu-id="b0058-107">*logMode*</span></span> 
</dt> <dd>

<span data-ttu-id="b0058-108">Обязательная строка, которая содержит буквы, представляющие типы сообщений для записи в журнал.</span><span class="sxs-lookup"><span data-stu-id="b0058-108">A required string that contains letters representing the message types to log.</span></span> <span data-ttu-id="b0058-109">Строка может быть сочетанием следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b0058-109">The string can be a combination of the following values.</span></span>



| <span data-ttu-id="b0058-110">Значение</span><span class="sxs-lookup"><span data-stu-id="b0058-110">Value</span></span> | <span data-ttu-id="b0058-111">Описание</span><span class="sxs-lookup"><span data-stu-id="b0058-111">Description</span></span>                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0058-112">I</span><span class="sxs-lookup"><span data-stu-id="b0058-112">I</span></span>     | <span data-ttu-id="b0058-113">Информационные сообщения.</span><span class="sxs-lookup"><span data-stu-id="b0058-113">Information-only messages.</span></span>                                                                             |
| <span data-ttu-id="b0058-114">w</span><span class="sxs-lookup"><span data-stu-id="b0058-114">w</span></span>     | <span data-ttu-id="b0058-115">Некритические предупреждающие сообщения.</span><span class="sxs-lookup"><span data-stu-id="b0058-115">Non-fatal warning messages.</span></span>                                                                            |
| <span data-ttu-id="b0058-116">й</span><span class="sxs-lookup"><span data-stu-id="b0058-116">e</span></span>     | <span data-ttu-id="b0058-117">Сообщения об ошибках, которые могут быть неустранимыми ошибками.</span><span class="sxs-lookup"><span data-stu-id="b0058-117">Error messages that may be fatal errors.</span></span>                                                               |
| <span data-ttu-id="b0058-118">f</span><span class="sxs-lookup"><span data-stu-id="b0058-118">f</span></span>     | <span data-ttu-id="b0058-119">Список используемых файлов, которые необходимо заменить.</span><span class="sxs-lookup"><span data-stu-id="b0058-119">List of files in use that need to be replaced.</span></span>                                                         |
| <span data-ttu-id="b0058-120">а</span><span class="sxs-lookup"><span data-stu-id="b0058-120">a</span></span>     | <span data-ttu-id="b0058-121">Уведомление о начале действия.</span><span class="sxs-lookup"><span data-stu-id="b0058-121">Start of action notification.</span></span>                                                                          |
| <span data-ttu-id="b0058-122">r</span><span class="sxs-lookup"><span data-stu-id="b0058-122">r</span></span>     | <span data-ttu-id="b0058-123">Запись данных действия, содержащая содержимое, относящееся к действию.</span><span class="sxs-lookup"><span data-stu-id="b0058-123">Action data record containing content specific to action.</span></span>                                              |
| <span data-ttu-id="b0058-124">u</span><span class="sxs-lookup"><span data-stu-id="b0058-124">u</span></span>     | <span data-ttu-id="b0058-125">Сообщения запроса пользователя.</span><span class="sxs-lookup"><span data-stu-id="b0058-125">User request messages.</span></span>                                                                                 |
| <span data-ttu-id="b0058-126">c</span><span class="sxs-lookup"><span data-stu-id="b0058-126">c</span></span>     | <span data-ttu-id="b0058-127">Параметры инициализации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b0058-127">UI initialization parameters.</span></span>                                                                          |
| <span data-ttu-id="b0058-128">m</span><span class="sxs-lookup"><span data-stu-id="b0058-128">m</span></span>     | <span data-ttu-id="b0058-129">Сообщение о нехватке памяти.</span><span class="sxs-lookup"><span data-stu-id="b0058-129">Out-of-memory message.</span></span>                                                                                 |
| <span data-ttu-id="b0058-130">v</span><span class="sxs-lookup"><span data-stu-id="b0058-130">v</span></span>     | <span data-ttu-id="b0058-131">Передает большой объем информации в файл журнала, который обычно не используется для пользователей.</span><span class="sxs-lookup"><span data-stu-id="b0058-131">Sends large amounts of information to log file not generally useful to users.</span></span> <span data-ttu-id="b0058-132">Может использоваться для поддержки.</span><span class="sxs-lookup"><span data-stu-id="b0058-132">May be used for support.</span></span> |
| <span data-ttu-id="b0058-133">p</span><span class="sxs-lookup"><span data-stu-id="b0058-133">p</span></span>     | <span data-ttu-id="b0058-134">Дамп таблицы свойств; "свойство = значение" при завершении ядра</span><span class="sxs-lookup"><span data-stu-id="b0058-134">Dump property table; "property = value" at engine termination</span></span>                                          |
| \+    | <span data-ttu-id="b0058-135">Добавление к существующему файлу журнала.</span><span class="sxs-lookup"><span data-stu-id="b0058-135">Append to existing log file.</span></span>                                                                           |
| <span data-ttu-id="b0058-136">!</span><span class="sxs-lookup"><span data-stu-id="b0058-136">!</span></span>     | <span data-ttu-id="b0058-137">Запись каждой строки в файл журнала.</span><span class="sxs-lookup"><span data-stu-id="b0058-137">Flush each line to the log file.</span></span>                                                                       |
| <span data-ttu-id="b0058-138">x</span><span class="sxs-lookup"><span data-stu-id="b0058-138">x</span></span>     | <span data-ttu-id="b0058-139">Дополнительные отладочные сведения.</span><span class="sxs-lookup"><span data-stu-id="b0058-139">Extra debugging information.</span></span> <span data-ttu-id="b0058-140">Этот параметр доступен только в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b0058-140">This option only available with Windows Server 2003.</span></span>                      |
| <span data-ttu-id="b0058-141">o</span><span class="sxs-lookup"><span data-stu-id="b0058-141">o</span></span>     | <span data-ttu-id="b0058-142">Сообщения о нехватке места на диске.</span><span class="sxs-lookup"><span data-stu-id="b0058-142">Out-of-disk-space messages.</span></span>                                                                            |



 

</dd> <dt>

<span data-ttu-id="b0058-143">*logFile*</span><span class="sxs-lookup"><span data-stu-id="b0058-143">*logFile*</span></span> 
</dt> <dd>

<span data-ttu-id="b0058-144">Обязательная строка, содержащая путь к создаваемому файлу журнала.</span><span class="sxs-lookup"><span data-stu-id="b0058-144">Required string containing the path to the log file to be created.</span></span> <span data-ttu-id="b0058-145">Чтобы отключить ведение журнала, используйте пустую строку ("").</span><span class="sxs-lookup"><span data-stu-id="b0058-145">Use an empty string ("") to turn off logging.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0058-146">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0058-146">Return value</span></span>

<span data-ttu-id="b0058-147">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b0058-147">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0058-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0058-148">Remarks</span></span>

<span data-ttu-id="b0058-149">Путь к расположению файла журнала должен уже существовать при использовании этого метода.</span><span class="sxs-lookup"><span data-stu-id="b0058-149">The path to the logfile location must already exist when using this method.</span></span> <span data-ttu-id="b0058-150">Установщик не создает структуру каталогов для файла журнала.</span><span class="sxs-lookup"><span data-stu-id="b0058-150">The Installer does not create the directory structure for the logfile.</span></span>

<span data-ttu-id="b0058-151">Параметры ведения журнала, заданные с помощью **EnableLog** , переопределяют все существующие параметры политики ведения журнала установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="b0058-151">The logging options set using **EnableLog** override any existing Windows Installer logging policy settings.</span></span>

<span data-ttu-id="b0058-152">По умолчанию журнал перезаписывает существующий файл журнала.</span><span class="sxs-lookup"><span data-stu-id="b0058-152">Logging overwrites an existing log file by default.</span></span> <span data-ttu-id="b0058-153">Для добавления к существующему файлу журнала необходимо использовать букву "+" в режиме ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="b0058-153">You must use the '+' letter in the logging mode to append to an existing log file.</span></span>

<span data-ttu-id="b0058-154">Параметр "!" не рекомендуется, так как он может значительно замедлять установку.</span><span class="sxs-lookup"><span data-stu-id="b0058-154">The '!' option is not recommended because it can significantly slow installation.</span></span> <span data-ttu-id="b0058-155">Этот параметр может быть полезен при отладке установки.</span><span class="sxs-lookup"><span data-stu-id="b0058-155">This option may be useful when debugging an installation.</span></span>

<span data-ttu-id="b0058-156">Следующий пример скрипта включает подробное ведение журнала для установки.</span><span class="sxs-lookup"><span data-stu-id="b0058-156">The following sample script turns on verbose logging for an installation.</span></span> <span data-ttu-id="b0058-157">В конце установки созданный файл журнала будет иметь значение c: \\ temp \\ install. log.</span><span class="sxs-lookup"><span data-stu-id="b0058-157">At the end of the installation, the generated log file will be at c:\\temp\\install.log.</span></span>


```VB
    Dim Installer
    Set Installer = CreateObject("WindowsInstaller.Installer")
    Installer.EnableLog "voicewarmup", "c:\temp\install.log"
    Installer.InstallProduct "\\server\share\products\sample\sample.msi"
```



## <a name="requirements"></a><span data-ttu-id="b0058-158">Требования</span><span class="sxs-lookup"><span data-stu-id="b0058-158">Requirements</span></span>



| <span data-ttu-id="b0058-159">Требование</span><span class="sxs-lookup"><span data-stu-id="b0058-159">Requirement</span></span> | <span data-ttu-id="b0058-160">Значение</span><span class="sxs-lookup"><span data-stu-id="b0058-160">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0058-161">Версия</span><span class="sxs-lookup"><span data-stu-id="b0058-161">Version</span></span><br/> | <span data-ttu-id="b0058-162">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b0058-162">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b0058-163">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b0058-163">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b0058-164">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="b0058-164">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="b0058-165">DLL</span><span class="sxs-lookup"><span data-stu-id="b0058-165">DLL</span></span><br/>     | <dl> <span data-ttu-id="b0058-166"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0058-166"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="b0058-167">IID</span><span class="sxs-lookup"><span data-stu-id="b0058-167">IID</span></span><br/>     | <span data-ttu-id="b0058-168">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b0058-168">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="b0058-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0058-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0058-170">Ведение журнала установщик Windows</span><span class="sxs-lookup"><span data-stu-id="b0058-170">Windows Installer Logging</span></span>](windows-installer-logging.md)
</dt> </dl>

 

 




