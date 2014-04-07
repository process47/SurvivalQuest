#!/usr/bin/env python
# -*- coding: utf-8 -*-

#Programme: Survivalor
#Auteur: Anton.M
#Date 07/04/14

class Heros:
	bonusForce=40
	bonusDefense=40
	bonusAgilite=60
	bonusKill=10
	
	def __init__(self, classe):
		self.vie=10
		self.score=0
		self.classe=classe
		self.agi=0
		self.force=0
		self.defense=0
		
		self.kill=0
		self.parade=0
		self.saut=0
		
		self.coins=0
		
		self.calculStat()

	def calculStat(self):
		if self.classe == "assassin":
			self.agi=6
			self.force=5
			self.defense=4
		elif self.classe == "barbare":
			self.agi=4
			self.force=6
			self.defense=5		
		elif self.classe == "chevalier":
			self.agi=5
			self.force=4
			self.defense=6
		elif self.classe == "guerrier":
			self.agi=5
			self.force=5
			self.defense=5			
	
	def tuerMonstre(self, nbMonstre):
		self.kill+=nbMonstre
		self.score+=(nbMonstre*bonusKill)
		
		if self.kill > bonusForce:
			self.kill-=bonusForce
			self.force+=1
			
		elif self.kill == bonusForce:
			self.kill=0
			self.force+=1
	
	def paradeProjectil(self):
		self.score+=1
		
	def sautMonstre(self):
		self.score+=1
	
	def destructionProjectil(self):
		self.score+=1
	
	#Retourne -1 si le joueur n'a plus de vie (par extension: game over).
	def majVie(self, nbVie):
		self.vie+=nbVie
		
		if self.vie < 1:
			return -1
		else:
			return 0
	
	def augPoints(self, nbPoints):
		self.score+=nbPoints
		
	#Coins peut etre negatif
	def majCoins(self, nbCoins):
		self.coins+=nbCoins
