---
description: Таблица ModuleSignature является обязательной таблицей.
ms.assetid: 09802282-72ad-43f1-8cce-4cdc68b01e87
title: Таблица ModuleSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d75e3bb013472c49d18fa44b840ce07b11728faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545682"
---
# <a name="modulesignature-table"></a>Таблица ModuleSignature

Таблица ModuleSignature является обязательной таблицей. Он содержит все сведения, необходимые для обнаружения модуля слияния. Средство слияния добавляет эту таблицу в MSI файл, если она еще не существует. Таблица ModuleSignature в модуле слияния содержит только одну строку, содержащую ModuleID, Language и Version. Однако таблица ModuleSignature в MSI-файле содержит строку, содержащую эту информацию для каждого файла. MSM, который был объединен в него.

Средства слияния и проверки проверьте таблицу ModuleSignature в MSI-файлах, чтобы определить наличие всех зависимых модулей слияния, необходимых текущему модулю слияния (см. [таблицу модуледепенденци](moduledependency-table.md)), а также сведения о том, был ли ранее объединен пакет установки с любыми конфликтующими модулями слияния (см. [таблицу модуликсклусион Table](moduleexclusion-table.md)).

Таблица ModuleSignature содержит следующие столбцы.



| Столбец   | Type                         | Ключ | Допускает значения NULL |
|----------|------------------------------|-----|----------|
| ModuleID | [Идентификатор](identifier.md) | Да   | Нет        |
| Язык | [Integer](integer.md)       | Да   | Нет        |
| Версия  | [Version](version.md)       |     | Нет        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID
</dt> <dd>

Идентификатор, который уникальным образом идентифицирует модуль слияния. Два модуля слияния не могут иметь одинаковый ModuleID, если только модуль слияния не полностью обратно совместим с его предшественником. Идентификатор GUID для этого поля можно создать с помощью служебной программы, такой как GUIDGEN. Столбец ModuleID является первичным ключом для таблицы, поэтому он должен соответствовать соглашению об именовании для [именования первичных ключей в базах данных модуля слияния](naming-primary-keys-in-merge-module-databases.md). Например, если понятное имя модуля слияния — MyLibrary, а GUID — {880DE2F0-CDD8-11D1-A849-006097ABDE17}, запись в столбце ModuleID становится MyLibrary. 880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Языке
</dt> <dd>

Идентификатор языка задает язык по умолчанию для модуля слияния. Идентификатор языка имеет десятичный формат, например, Английский (США) — 1033. Язык, используемый модулем слияния, можно изменить, применив преобразование к модулю слияния перед слиянием.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>Версия
</dt> <dd>

Поле Version содержит строку, описывающую основную и дополнительную версии модуля слияния.

</dd> </dl>

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

## <a name="related-topics"></a>См. также

<dl> <dt>

[Модули слияния с несколькими языками](multiple-language-merge-modules.md)
</dt> </dl>

 

 



