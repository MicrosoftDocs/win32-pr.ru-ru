---
description: Метод Реинсталлпродукт объекта Installer переустанавливает продукт или устраняет проблемы установки в установленном продукте.
ms.assetid: ff933cce-9f27-4215-9291-dd860d9c4d08
title: Метод Installer. Реинсталлпродукт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ReinstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2cc10422657ffa1b2c15f1550f20feab3e378f0ec4b88a774f5faa297c49b0ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129344"
---
# <a name="installerreinstallproduct-method"></a>Метод Installer. Реинсталлпродукт

Метод **реинсталлпродукт** объекта [**Installer**](installer-object.md) переустанавливает продукт или устраняет проблемы установки в установленном продукте.

## <a name="syntax"></a>Синтаксис


```JScript
Installer.ReinstallProduct(
  Product,
  ReinstallMode
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Продукт* 
</dt> <dd>

Указывает код продукта.

</dd> <dt>

*ReinstallMode* 
</dt> <dd>

Указывает тип переустановки. Этот параметр может принимать одно или несколько следующих значений.



| Значение                                                                                                                                                                                                                                                                    | Значение                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="msiReinstallModeFileMissing"></span><span id="msireinstallmodefilemissing"></span><span id="MSIREINSTALLMODEFILEMISSING"></span><dl> <dt>**мсиреинсталлмодефилемиссинг**</dt> </dl>                     | Переустанавливает только в том случае, если файл отсутствует.<br/>                                |
| <span id="msiReinstallModeFileOlderVersion"></span><span id="msireinstallmodefileolderversion"></span><span id="MSIREINSTALLMODEFILEOLDERVERSION"></span><dl> <dt>**мсиреинсталлмодефилеолдерверсион**</dt> </dl> | Переустанавливает, если файл отсутствует или имеет более раннюю версию.<br/>              |
| <span id="msiReinstallModeFileEqualVersion"></span><span id="msireinstallmodefileequalversion"></span><span id="MSIREINSTALLMODEFILEEQUALVERSION"></span><dl> <dt>**мсиреинсталлмодефиликуалверсион**</dt> </dl> | Переустанавливает, если файл отсутствует или имеет такую же или более старую версию.<br/>     |
| <span id="msiReinstallModeFileExact"></span><span id="msireinstallmodefileexact"></span><span id="MSIREINSTALLMODEFILEEXACT"></span><dl> <dt>**мсиреинсталлмодефиликсакт**</dt> </dl>                             | Переустанавливает, если файл отсутствует или не является точной версией.<br/>          |
| <span id="msiReinstallModeFileVerify"></span><span id="msireinstallmodefileverify"></span><span id="MSIREINSTALLMODEFILEVERIFY"></span><dl> <dt>**мсиреинсталлмодефилеверифи**</dt> </dl>                         | Проверяет исполняемые файлы и переустанавливает их, если они отсутствуют или повреждены.<br/> |
| <span id="msiReinstallModeFileReplace"></span><span id="msireinstallmodefilereplace"></span><span id="MSIREINSTALLMODEFILEREPLACE"></span><dl> <dt>**мсиреинсталлмодефилереплаце**</dt> </dl>                     | Переустанавливает все файлы независимо от версии.<br/>                            |
| <span id="msiReinstallModeUserData"></span><span id="msireinstallmodeuserdata"></span><span id="MSIREINSTALLMODEUSERDATA"></span><dl> <dt>**мсиреинсталлмодеусердата**</dt> </dl>                                 | Проверяет наличие записей реестра, необходимых для пользователя.<br/>                            |
| <span id="msiReinstallModeMachineData"></span><span id="msireinstallmodemachinedata"></span><span id="MSIREINSTALLMODEMACHINEDATA"></span><dl> <dt>**мсиреинсталлмодемачинедата**</dt> </dl>                     | Проверяет наличие записей реестра, необходимых для каждого компьютера.<br/>                         |
| <span id="msiReinstallModeShortcut"></span><span id="msireinstallmodeshortcut"></span><span id="MSIREINSTALLMODESHORTCUT"></span><dl> <dt>**мсиреинсталлмодешорткут**</dt> </dl>                                 | Проверяет сочетания клавиш.<br/>                                                   |
| <span id="msiReinstallModePackage"></span><span id="msireinstallmodepackage"></span><span id="MSIREINSTALLMODEPACKAGE"></span><dl> <dt>**мсиреинсталлмодепаккаже**</dt> </dl>                                     | Использует источник повторного кэширования для установки пакета.<br/>                        |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>См. также

<dl> <dt>

[**мсиреинсталлпродукт**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
</dt> <dt>

[Функции установки и настройки](installer-function-reference.md)
</dt> </dl>

 

 




