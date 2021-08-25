---
description: Таблица Ккпсеарч содержит список подписей файлов, используемых для программы проверки соответствия (CCP). По крайней мере один из этих файлов должен присутствовать на компьютере пользователя, чтобы пользователь был в соответствии с программой.
ms.assetid: 98d21e24-1633-44b7-bfdb-5a40bab8d319
title: Таблица Ккпсеарч
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d20894960dce7f346601bd2ed459140caa305323ca02d14d54416f32737216
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821844"
---
# <a name="ccpsearch-table"></a>Таблица Ккпсеарч

Таблица Ккпсеарч содержит список подписей файлов, используемых для программы проверки соответствия (CCP). По крайней мере один из этих файлов должен присутствовать на компьютере пользователя, чтобы пользователь был в соответствии с программой.

Таблица Ккпсеарч содержит следующий столбец.



| Столбец      | Type                         | Ключ | Допускает значения NULL |
|-------------|------------------------------|-----|----------|
| Образец\_ | [Идентификатор](identifier.md) | Д   | Нет        |



 

## <a name="column"></a>Столбец

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Образец\_
</dt> <dd>

Сигнатура \_ представляет собой уникальную сигнатуру файла и является также внешним ключом в таблицах [Signature](signature-table.md), [реглокатор](reglocator-table.md), [инилокатор](inilocator-table.md), [комплокатор](complocator-table.md)и [дрлокатор](drlocator-table.md) .

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта таблица упоминается при выполнении [действия ккпсеарч](ccpsearch-action.md) или [рмккпсеарч](rmccpsearch-action.md) .

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



