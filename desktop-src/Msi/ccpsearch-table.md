---
description: Таблица Ккпсеарч содержит список подписей файлов, используемых для программы проверки соответствия (CCP). По крайней мере один из этих файлов должен присутствовать на компьютере пользователя, чтобы пользователь был в соответствии с программой.
ms.assetid: 98d21e24-1633-44b7-bfdb-5a40bab8d319
title: Таблица Ккпсеарч
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368c0452fea011aca1080ca17020467ba6e0dc4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662911"
---
# <a name="ccpsearch-table"></a>Таблица Ккпсеарч

Таблица Ккпсеарч содержит список подписей файлов, используемых для программы проверки соответствия (CCP). По крайней мере один из этих файлов должен присутствовать на компьютере пользователя, чтобы пользователь был в соответствии с программой.

Таблица Ккпсеарч содержит следующий столбец.



| Столбец      | Type                         | Ключ | Допускает значения NULL |
|-------------|------------------------------|-----|----------|
| Образец\_ | [Идентификатор](identifier.md) | Да   | Нет        |



 

## <a name="column"></a>Столбец

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Образец\_
</dt> <dd>

Сигнатура \_ представляет собой уникальную сигнатуру файла и является также внешним ключом в таблицах [Signature](signature-table.md), [реглокатор](reglocator-table.md), [инилокатор](inilocator-table.md), [комплокатор](complocator-table.md)и [дрлокатор](drlocator-table.md) .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эта таблица упоминается при выполнении [действия ккпсеарч](ccpsearch-action.md) или [рмккпсеарч](rmccpsearch-action.md) .

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



