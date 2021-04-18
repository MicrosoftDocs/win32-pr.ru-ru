---
description: Метод Форматрекорд объекта Session возвращает форматированную строку из шаблона и данные записи.
ms.assetid: 2018ac75-ea18-4256-8d56-0527069ce24b
title: Session. Форматрекорд, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FormatRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e87c73e5ef7adafd9caab00bf257fe8a7afc3c33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675424"
---
# <a name="sessionformatrecord-method"></a><span data-ttu-id="0aab0-103">Session. Форматрекорд, метод</span><span class="sxs-lookup"><span data-stu-id="0aab0-103">Session.FormatRecord method</span></span>

<span data-ttu-id="0aab0-104">Метод **форматрекорд** объекта [**Session**](session-object.md) Возвращает форматированную строку из шаблона и данные записи.</span><span class="sxs-lookup"><span data-stu-id="0aab0-104">The **FormatRecord** method of the [**Session**](session-object.md) object returns a formatted string from a template and record data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aab0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0aab0-105">Syntax</span></span>


```JScript
Session.FormatRecord(
  record
)
```



## <a name="parameters"></a><span data-ttu-id="0aab0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0aab0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aab0-107">*record*</span><span class="sxs-lookup"><span data-stu-id="0aab0-107">*record*</span></span> 
</dt> <dd>

<span data-ttu-id="0aab0-108">Обязательный объект **Record** , содержащий шаблон и данные для форматирования.</span><span class="sxs-lookup"><span data-stu-id="0aab0-108">Required **Record** object containing a template and data to be formatted.</span></span> <span data-ttu-id="0aab0-109">Строка шаблона должна быть задана в поле 0, за которым следуют все параметры данных, на которые указывают ссылки.</span><span class="sxs-lookup"><span data-stu-id="0aab0-109">The template string must be set in field 0 followed by any referenced data parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0aab0-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0aab0-110">Return value</span></span>

<span data-ttu-id="0aab0-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0aab0-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0aab0-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0aab0-112">Remarks</span></span>

<span data-ttu-id="0aab0-113">Метод **форматрекорд** использует следующий процесс форматирования.</span><span class="sxs-lookup"><span data-stu-id="0aab0-113">The **FormatRecord** method uses the following format process.</span></span>

<span data-ttu-id="0aab0-114">Параметры для [форматирования](formatted.md) заключаются в квадратные скобки \[ .. \] .</span><span class="sxs-lookup"><span data-stu-id="0aab0-114">Parameters to be [formatted](formatted.md) are enclosed in square brackets \[..\].</span></span> <span data-ttu-id="0aab0-115">Можно выполнить итерацию квадратных скобок, так как подстановки разрешаются из внутренней области.</span><span class="sxs-lookup"><span data-stu-id="0aab0-115">The square brackets can be iterated because the substitutions are resolved from inside out.</span></span>

<span data-ttu-id="0aab0-116">Если часть строки заключена в фигурные скобки {} и не содержит квадратных скобок, часть остается без изменений, включая фигурные скобки.</span><span class="sxs-lookup"><span data-stu-id="0aab0-116">If a part of the string is enclosed in curly braces { } and contains no square brackets, the part is left unchanged, including the curly braces.</span></span>

<span data-ttu-id="0aab0-117">Если часть строки заключена в фигурные скобки и содержит одно или несколько имен свойств, и если все свойства найдены, текст (с разрешенными подстановками) отображается без фигурных скобок.</span><span class="sxs-lookup"><span data-stu-id="0aab0-117">If a part of the string is enclosed in curly braces and contains one or more property names, and if all the properties are found, the text (with the resolved substitutions) is displayed without the curly braces.</span></span> <span data-ttu-id="0aab0-118">Если какое бы то ни было свойство не найдено, все тексты фигурных скобок и фигурных скобок удаляются.</span><span class="sxs-lookup"><span data-stu-id="0aab0-118">If any of the properties are not found, all the text in the curly braces and the braces themselves are removed.</span></span>

<span data-ttu-id="0aab0-119">**Форматирование строк с помощью метода Форматрекорд**</span><span class="sxs-lookup"><span data-stu-id="0aab0-119">**To format strings using the FormatRecord method**</span></span>

1.  <span data-ttu-id="0aab0-120">Числовые параметры заменяются путем замены маркера значением соответствующего поля записи с отсутствующими или нулевыми значениями, не создающими никакого текста.</span><span class="sxs-lookup"><span data-stu-id="0aab0-120">The numeric parameters are substituted by replacing the marker with the value of the corresponding record field, with missing or Null values producing no text.</span></span>
2.  <span data-ttu-id="0aab0-121">Строка, которая обрабатывается в результате замены параметров, не относящихся от записи, соответствующими значениями, как указано в следующих описаниях.</span><span class="sxs-lookup"><span data-stu-id="0aab0-121">The string that results is processed by replacing the non-record parameters with the corresponding values, as noted in the following descriptions.</span></span>
    -   <span data-ttu-id="0aab0-122">Если обнаружена подстрока формы « \[ PropertyName \] », она заменяется значением свойства.</span><span class="sxs-lookup"><span data-stu-id="0aab0-122">If a substring of the form "\[propertyname\]" is encountered, it is replaced by the value of the property.</span></span>
    -   <span data-ttu-id="0aab0-123">При обнаружении подстроки вида " \[ % environmentvariable \] " значение переменной среды подставляется.</span><span class="sxs-lookup"><span data-stu-id="0aab0-123">If a substring of the form "\[%environmentvariable\]" is found, the value of the environment variable is substituted.</span></span>
    -   <span data-ttu-id="0aab0-124">Если подстрока формы \[ \# *филекэй* \] найдена, она заменяется полным путем к файлу со значением *филекэй* , используемым в качестве ключа в [таблице File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="0aab0-124">If a substring of the form \[\#*filekey*\] is found, it is replaced by the full path of the file, with the value *filekey* used as a key into the [File table](file-table.md).</span></span> <span data-ttu-id="0aab0-125">Значение \[ \# *филекэй* \] остается пустым и не заменяется путем, пока установщик не выполнит действие [костинитиализе](costinitialize-action.md), [филекост Action](filecost-action.md)и [костфинализе](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="0aab0-125">The value of \[\#*filekey*\] remains blank and is not replaced by a path until the installer runs the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="0aab0-126">Значение \[ \# *филекэй* \] зависит от состояния установки компонента, которому принадлежит файл.</span><span class="sxs-lookup"><span data-stu-id="0aab0-126">The value of \[\#*filekey*\] depends upon the installation state of the component to which the file belongs.</span></span> <span data-ttu-id="0aab0-127">Если компонент запускается из источника, значением является путь к исходному расположению файла.</span><span class="sxs-lookup"><span data-stu-id="0aab0-127">If the component is being run from source, the value is the path to the source location of the file.</span></span> <span data-ttu-id="0aab0-128">Если компонент выполняется локально, значение представляет собой путь к целевому расположению файла после установки.</span><span class="sxs-lookup"><span data-stu-id="0aab0-128">If the component is being run locally, the value is the path to the target location of the file after installation.</span></span> <span data-ttu-id="0aab0-129">Если компонент отсутствует, путь будет пустым.</span><span class="sxs-lookup"><span data-stu-id="0aab0-129">If the component is absent, the path is blank.</span></span> <span data-ttu-id="0aab0-130">Дополнительные сведения о проверке состояния установки компонентов см. [в разделе Проверка установки компонентов, компонентов и файлов](checking-the-installation-of-features-components-files.md).</span><span class="sxs-lookup"><span data-stu-id="0aab0-130">For more information about checking the installation state of components, see [Checking the Installation of Features, Components, Files](checking-the-installation-of-features-components-files.md).</span></span>
    -   <span data-ttu-id="0aab0-131">Если подстрока формы \[ *$componentkey* \] найдена, она заменяется каталогом установки компонента со значением *компоненткэй* , используемым в качестве ключа в [таблице Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="0aab0-131">If a substring of the form \[*$componentkey*\] is found, it is replaced by the install directory of the component, with the value *componentkey* used as a key into the [Component table](component-table.md).</span></span> <span data-ttu-id="0aab0-132">Значение \[ $ *компоненткэй* \] остается пустым и не заменяется каталогом, пока установщик не выполнит действие [костинитиализе](costinitialize-action.md), [филекост Action](filecost-action.md)и [костфинализе](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="0aab0-132">The value of \[$*componentkey*\] remains blank and is not replaced by a directory until the installer runs the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="0aab0-133">Значение \[ $ *компоненткэй* \] зависит от состояния установки компонента.</span><span class="sxs-lookup"><span data-stu-id="0aab0-133">The value of \[$*componentkey*\] depends upon the installation state of the component.</span></span> <span data-ttu-id="0aab0-134">Если компонент запускается из источника, значение является исходным каталогом файла.</span><span class="sxs-lookup"><span data-stu-id="0aab0-134">If the component is being run from source, the value is the source directory of the file.</span></span> <span data-ttu-id="0aab0-135">Если компонент выполняется локально, значение является целевым каталогом после установки.</span><span class="sxs-lookup"><span data-stu-id="0aab0-135">If the component is being run locally, the value is the target directory after installation.</span></span> <span data-ttu-id="0aab0-136">Если компонент отсутствует, значение остается пустым.</span><span class="sxs-lookup"><span data-stu-id="0aab0-136">If the component is absent, the value is left blank.</span></span> <span data-ttu-id="0aab0-137">Дополнительные сведения о проверке состояния установки компонентов см. [в разделе Проверка установки компонентов, компонентов и файлов](checking-the-installation-of-features-components-files.md).</span><span class="sxs-lookup"><span data-stu-id="0aab0-137">For more information about checking the installation state of components, see [Checking the Installation of Features, Components, Files](checking-the-installation-of-features-components-files.md).</span></span>
    -   <span data-ttu-id="0aab0-138">Если подстрока формы " \[ \\ c \] " найдена, она заменяется символом без дальнейшей обработки.</span><span class="sxs-lookup"><span data-stu-id="0aab0-138">If a substring of the form "\[\\c\]" is found, it is replaced by the character without any further processing.</span></span> <span data-ttu-id="0aab0-139">Сохраняется только первый символ после обратной косой черты; все остальное удаляется.</span><span class="sxs-lookup"><span data-stu-id="0aab0-139">Only the first character after the backslash is kept; everything else is removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aab0-140">Требования</span><span class="sxs-lookup"><span data-stu-id="0aab0-140">Requirements</span></span>



| <span data-ttu-id="0aab0-141">Требование</span><span class="sxs-lookup"><span data-stu-id="0aab0-141">Requirement</span></span> | <span data-ttu-id="0aab0-142">Значение</span><span class="sxs-lookup"><span data-stu-id="0aab0-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aab0-143">Версия</span><span class="sxs-lookup"><span data-stu-id="0aab0-143">Version</span></span><br/> | <span data-ttu-id="0aab0-144">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0aab0-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0aab0-145">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0aab0-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0aab0-146">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="0aab0-146">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0aab0-147">DLL</span><span class="sxs-lookup"><span data-stu-id="0aab0-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="0aab0-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0aab0-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0aab0-149">IID</span><span class="sxs-lookup"><span data-stu-id="0aab0-149">IID</span></span><br/>     | <span data-ttu-id="0aab0-150">IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0aab0-150">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="0aab0-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0aab0-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aab0-152">Формате</span><span class="sxs-lookup"><span data-stu-id="0aab0-152">Formatted</span></span>](formatted.md)
</dt> <dt>

[<span data-ttu-id="0aab0-153">Типы данных столбцов</span><span class="sxs-lookup"><span data-stu-id="0aab0-153">Column Data Types</span></span>](column-data-types.md)
</dt> </dl>

 

 




