---
description: Метод Реинсталлфеатуре объекта Installer переустанавливает компоненты или устраняет проблемы с установленными компонентами.
ms.assetid: cfe2aef4-7742-49cd-b7a3-7d484e1f85e3
title: Метод Installer. Реинсталлфеатуре
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ReinstallFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: dfe4cb96ccac85fb5b94f3a2a8ec3dcca48f6fa4300a6bceb338b2ebbe01da22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946290"
---
# <a name="installerreinstallfeature-method"></a>Метод Installer. Реинсталлфеатуре

Метод **реинсталлфеатуре** объекта [**Installer**](installer-object.md) переустанавливает компоненты или устраняет проблемы с установленными компонентами.

## <a name="syntax"></a>Синтаксис


```JScript
Installer.ReinstallFeature(
  Product,
  Feature,
  ReinstallMode
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Продукт* 
</dt> <dd>

Указывает код продукта.

</dd> <dt>

*Компонент* 
</dt> <dd>

Указывает компонент для переустановки. Родительский компонент или дочерний компонент указанного компонента не переустановлен. Чтобы переустановить родительскую или дочернюю функцию, необходимо вызвать метод **реинсталлфеатуре** отдельно или использовать метод [**реинсталлпродукт**](installer-reinstallproduct.md) .

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>См. также

<dl> <dt>

[**мсиреинсталлфеатуре**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
</dt> <dt>

[Функции установки и настройки](installer-function-reference.md)
</dt> </dl>

 

 




