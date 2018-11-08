Remove Foreign Key Constraint !!!!!!


-- --------------------------------------------------------
-- Host:                         192.168.100.240
-- Server Version:               5.1.73 - Source distribution
-- Server Betriebssystem:        redhat-linux-gnu
-- HeidiSQL Version:             9.5.0.5196
-- --------------------------------------------------------

/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET NAMES utf8 */;
/*!40014 SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0 */;
/*!40101 SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='NO_AUTO_VALUE_ON_ZERO' */;

-- Exportiere Struktur von Tabelle asterisk.buttonconfig
DROP TABLE IF EXISTS `buttonconfig`;
CREATE TABLE IF NOT EXISTS `buttonconfig` (
  `device` varchar(15) NOT NULL DEFAULT '',
  `instance` tinyint(4) NOT NULL DEFAULT '0',
  `type` enum('line','speeddial','service','feature','empty') NOT NULL DEFAULT 'line',
  `name` varchar(36) DEFAULT NULL,
  `options` varchar(100) DEFAULT NULL,
  PRIMARY KEY (`device`,`instance`,`type`),
  KEY `device` (`device`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

-- Exportiere Daten aus Tabelle asterisk.buttonconfig: ~18 rows (ungefähr)
/*!40000 ALTER TABLE `buttonconfig` DISABLE KEYS */;
REPLACE INTO `buttonconfig` (`device`, `instance`, `type`, `name`, `options`) VALUES
	('SEP8CB64FF7B966', 1, 'line', '12', 'default'),
	('SEP8CB64FF7B966', 2, 'speeddial', 'Anmeldung', '11,11@ext-local'),
	('SEP8CB64FF7B966', 3, 'speeddial', 'Sprechzimmer 2', '14,14@ext-local'),
	('SEP8CB64FF7B966', 4, 'speeddial', 'AN: hohes Aufkom.', '*282,*282@app-daynight-toggle'),
	('SEP8CB64FF7B966', 5, 'speeddial', 'AN: Urlaub', '*280,*280@app-daynight-toggle'),
	('SEP8CB64FF7B966', 6, 'speeddial', 'AN: Geschlossen', '*281,*281@app-daynight-toggle'),
	('SEP9CAFCA85407A', 1, 'line', '11', 'default'),
	('SEP9CAFCA85407A', 2, 'speeddial', 'Backoffice', '12,12@ext-local'),
	('SEP9CAFCA85407A', 3, 'speeddial', 'Sprechzimmer 2', '14,14@ext-local'),
	('SEP9CAFCA85407A', 4, 'speeddial', 'AN: hohes Aufkom.', '*282,*282@app-daynight-toggle'),
	('SEP9CAFCA85407A', 5, 'speeddial', 'AN: Urlaub', '*280,*280@app-daynight-toggle'),
	('SEP9CAFCA85407A', 6, 'speeddial', 'AN: Geschlossen', '*281,*281@app-daynight-toggle'),
	('SEPF47F35A2669D', 1, 'line', '14', 'default'),
	('SEPF47F35A2669D', 2, 'speeddial', 'Backoffice', '12,12@ext-local'),
	('SEPF47F35A2669D', 3, 'speeddial', 'Anmeldung', '11,11@ext-local'),
	('SEPF47F35A2669D', 4, 'empty', '', ''),
	('SEPF47F35A2669D', 5, 'empty', '', ''),
	('SEPF47F35A2669D', 6, 'line', '21', '');
/*!40000 ALTER TABLE `buttonconfig` ENABLE KEYS */;

/*!40101 SET SQL_MODE=IFNULL(@OLD_SQL_MODE, '') */;
/*!40014 SET FOREIGN_KEY_CHECKS=IF(@OLD_FOREIGN_KEY_CHECKS IS NULL, 1, @OLD_FOREIGN_KEY_CHECKS) */;
/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
